     fd6        if   e             disk    rename(d6:d6f) prefix(x)
     dst               s           4095
     dsu               S             14
     dsue              s              1
     dsus              s             14
     derg              s              4  0
     dt                s              4  0 INZ(1)
     di                s              2  0
     c                   read      d6f
     c                   eval      st=xd6
     c                   for       t = 1 to 4091
     c                   eval      su=%SUBST(st:t:14)
     c                   for       i = 1 to 14
     c                   eval      sue=%SUBST(su:i:1)
     c                   eval      sus=%REPLACE('_':su:i:1)
     c                   eval      erg=%SCAN(sue:sus:1)
     c
     c                   if        erg>0
     c                   setoff                                       21
     c                   endif
     c                   endfor
     c                   if        *in21 = *on
     c                   eval      t=t+13
     c     t             dsply
     c                   endif
     c                   seton                                            21
     c                   endfor
     c                   seton                                            LR

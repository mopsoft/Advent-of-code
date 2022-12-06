     fd6        if   e             disk    rename(d6:d6f) prefix(x)
     dsu               S              4
     dsue              s              1
     dsus              s              4
     dst               s           4095
     derg              s              4  0
     dt                s              4  0 INZ(1)
     di                s              1  0
     c                   read      d6f
     c                   eval      st=xd6
     c                   for       t = 1 to 4091
     c                   eval      su=%SUBST(st:t:4)
     c                   for       i = 1 to 4
     c                   eval      sue=%SUBST(su:i:1)
     c                   eval      sus=%REPLACE('_':su:i:1)
     c                   eval      erg=%SCAN(sue:sus:1)
     c                   if        erg>0
     c                   setoff                                       21
     c                   endif
     c                   endfor
     c                   if        *in21 = *on
     c                   eval      t=t+3
     c     t             dsply
     c                   endif
     c                   seton                                            21
     c                   endfor
     c                   seton                                            LR

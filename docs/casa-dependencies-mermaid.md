# CASA C++ Dependencies Map

   This is a visual representation of the dependencies from `casacpp_deps.dot`.

   ```mermaid
   graph TD
       subgraph "External Deps"
           bisonflex["bison/flex"]
           casacore
           libsakura
           libxmlpp["libxml++"]
           fftw
           gsl
           grpc
           mirlib
           mpi
           rpfits["rpfits (embedded)"]
           sqlite
           wcslib
       end

       subgraph "CASA Deps"
           alma
           asdmstman
           atnf
           calanalysis
           casa_sakura
           casatools
           components
           flagging
           imageanalysis
           miriad
           mstransform
           msvis
           nrao
           parallel
           singledish
           singledishfiller
           spectrallines
           stdcasa
           synthesis

           alma --> casacore
           alma --> libxmlpp
           asdmstman --> casacore
           atnf --> casacore
           atnf --> rpfits
           calanalysis --> synthesis
           calanalysis --> casacore
           casa_sakura --> libsakura
           casatools --> grpc
           casatools --> casacore
           components --> casatools
           components --> stdcasa
           components --> casacore
           components --> gsl
           flagging --> casatools
           flagging --> msvis
           flagging --> mstransform
           flagging --> stdcasa
           flagging --> synthesis
           flagging --> casacore
           flagging --> grpc
           imageanalysis --> components
           imageanalysis --> stdcasa
           miriad --> casacore
           miriad --> mirlib
           mstransform --> asdmstman
           mstransform --> atmosphere
           mstransform --> imageanalysis
           mstransform --> msvis
           mstransform --> stdcasa
           mstransform --> gsl
           mstransform --> wcslib
           msvis --> asdmstman
           msvis --> components
           msvis --> stdcasa
           msvis --> casacore
           nrao --> casacore
           parallel --> casacore
           singledish --> casa_sakura
           singledish --> mstransform
           singledish --> msvis
           singledish --> singledishfiller
           singledish --> stdcasa
           singledish --> casacore
           singledish --> libsakura
           singledishfiller --> casacore
           spectrallines --> casatools
           spectrallines --> imageanalysis
           spectrallines --> casacore
           spectrallines --> sqlite
           stdcasa --> casacore
           synthesis --> atmosphere
           synthesis --> casadbus
           synthesis --> casatools
           synthesis --> components
           synthesis --> graphics
           synthesis --> imageanalysis
           synthesis --> msvis
           synthesis --> mstransform
           synthesis --> stdcasa
           synthesis --> casacore
           synthesis --> bisonflex
           synthesis --> fftw
           synthesis --> grpc
           synthesis --> gsl
           synthesis --> libsakura
           synthesis --> mpi
           synthesis --> wcslib
       end
   ```
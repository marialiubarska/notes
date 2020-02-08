# Event generation 

## GENIE-IceTray

generator app: `I3GENIEGenerator.cxx`

generation:

1. In `I3GENIEGenerator.cxx` call ``



## ext-genie-icetray

generation app: `genie-generator/genie/gIceCubeEvGen.cxx`:

 
`int main(int argc, char ** argv)`

    GetCommandLineArgs(argc,argv);
    FillCommandLineArgsDict();
    Initialize();

    void GenerateEventsUsingFluxOrTgtMix(void)
    
```
   // Create the monte carlo job driver
   GMCJDriver * mcj_driver = new GMCJDriver;
   //  mcj_driver->SetEventGeneratorList(RunOpt::Instance()->EventGeneratorList());
   //  mcj_driver->SetUnphysEventMask(*RunOpt::Instance()->UnphysEventMask());
   mcj_driver->UseFluxDriver(flux_driver);
   mcj_driver->UseGeomAnalyzer(geom_driver);
   mcj_driver->UseSplines();
   if(gOptSingleProbScale) 
   mcj_driver->ForceSingleProbScale(); // do not set this if weighted events should be generated
   mcj_driver->KeepOnThrowingFluxNeutrinos(true); // always return a neutrino
   mcj_driver->Configure();
```
      
       



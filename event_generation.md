# Event generation 

## GENIE-IceTray

generator app: `I3GENIEGenerator.cxx`

generation:

1. In `I3GENIEGenerator.cxx` call ``



## ext-genie-icetray

generation app: `genie-generator/genie/gIceCubeEvGen.cxx`:

 ```
 int main(int argc, char ** argv)
{
  GetCommandLineArgs(argc,argv);
  FillCommandLineArgsDict();
  Initialize();
  ...
  GenerateEventsUsingFluxOrTgtMix();
  ...
  return 0;
}
 ```


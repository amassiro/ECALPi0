# ECALPi0
ECAL Pi0 Calibration


where:

    /home/amassiro/Cern/Code/ECAL/ECALPi0
    /afs/cern.ch/user/a/amassiro/work/ECAL/CMSSW_7_4_0_pre6/src/CalibCode/submit
    
    /afs/cern.ch/user/a/amassiro/work/ECAL/CMSSW_7_4_2
    
Instructions:

    https://indico.cern.ch/event/381010/contribution/0/material/slides/0.pdf
    
    
    git clone git@github.com:lpernie/ECALpro.git CalibCode
    scram b -j 12
    cd CalibCode/submit
    chmod +x submitCalibration.py resubmitCalibration.py

    cd ..
    cd FillEpsilonPlot/test/
    
    cmsRun fillepsilonplot_cfg.py inputFiles=file:/tmp/amassiro/outputALCAP0_6_1_N7w.root    outputFile=/tmp/amassiro/

Pi0 code:

    https://github.com/ECALELFS/ECALpro

    
    
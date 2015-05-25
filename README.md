# ECALPi0
ECAL Pi0 Calibration


where:

    /home/amassiro/Cern/Code/ECAL/ECALPi0

    /afs/cern.ch/user/a/amassiro/work/ECAL/CMSSW_7_4_0_pre6/src/CalibCode/submit    
    /afs/cern.ch/user/a/amassiro/work/ECAL/CMSSW_7_4_2  ---> problem with multifit
    /afs/cern.ch/user/a/amassiro/work/ECAL/CMSSW_7_4_0_pre8/src/CalibCode/submit

    
Instructions:

    https://indico.cern.ch/event/381010/contribution/0/material/slides/0.pdf
    
    
    git clone git@github.com:lpernie/ECALpro.git CalibCode
    scram b -j 12
    cd CalibCode/submit
    chmod +x submitCalibration.py resubmitCalibration.py
    ./submitCalibration.py    ----> to create a bunch of test python files

    cd ..
    cd FillEpsilonPlot/test/
    
    cmsRun fillepsilonplot_cfg.py inputFiles=file:/tmp/amassiro/outputALCAP0_6_1_N7w.root    outputFile=/tmp/amassiro/

    cp /afs/cern.ch/user/l/lpernie/public/4AndreaM/calibMap.root ../data/
    cp /afs/cern.ch/user/l/lpernie/public/4AndreaM/caloGeometry.root ../data/
    
    cmsRun example.py \
        inputFiles=root://eoscms//eos/cms/store/group/dpg_ecal/alca_ecalcalib/hardenbr/STREAM_OUTPUT/NEU_GUN_40bx25_WITH_SELECTION_NOL1/outputALCAP0_1000_1_0jE.root   \
        outputFile=/tmp/amassiro/
    
    eos cp /eos/cms/store/group/dpg_ecal/alca_ecalcalib/hardenbr/OPTIM_NTUPLES/MINBIAS_PIZERO_ALCARAW_NOUNCAL_NOL1FILTER_40bx50_WITHSELECTION_WITHGEN_WITHRECHIT/outputALCAP0_363_1_jme.root /tmp/amassiro/
    cmsRun example.py \
        inputFiles=file:/tmp/amassiro/outputALCAP0_363_1_jme.root \
        outputFile=/tmp/amassiro/
    
    
    
    
Pi0 code:

    https://github.com/ECALELFS/ECALpro

    
    
    
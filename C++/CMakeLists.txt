#
# Copyright (c) Reliable Robotics Corporation.
# All Rights Reserved.
#

include_directories(include)

add_compile_options(
    -Wall
    -O
    -fPIC
)

add_subdirectory(src)

# Set `HEADERS` to the list of all *.h files in
# this directory. We will include these headers 
# in the Daidalus library install.
set(HEADERS
    include/Daidalus.h
    include/ACCoRDConfig.h
    include/AircraftState.h
    include/Alerter.h
    include/AlertThresholds.h
    include/AziEquiProjection.h
    include/BandsCore.h
    include/Bands.h
    include/BandsHysteresis.h
    include/BandsMofN.h
    include/BandsRange.h
    include/BandsRegion.h
    include/CD2D.h
    include/CD3D.h
    include/CDCylinder.h
    include/ColorValue.h
    include/ConflictData.h
    include/Constants.h
    include/Consts.h
    include/CriteriaCore.h
    include/Criteria.h
    include/CriticalVectors2D.h
    include/CriticalVectors.h
    include/DaidalusAltBands.h
    include/DaidalusCore.h
    include/DaidalusDirBands.h
    include/DaidalusFileWalker.h
    include/Daidalus.h
    include/DaidalusHsBands.h
    include/DaidalusIntegerBands.h
    include/DaidalusParameters.h
    include/DaidalusRealBands.h
    include/DaidalusVsBands.h
    include/DCPAUrgencyStrategy.h
    include/Debug.h
    include/Detection3DAcceptor.h
    include/Detection3D.h
    include/Detection3DParameterReader.h
    include/Detection3DParameterWriter.h
    include/Detection3DResAcceptor.h
    include/ENUProjection.h
    include/ErrorLog.h
    include/ErrorReporter.h
    include/EuclideanProjection.h
    include/FixedAircraftUrgencyStrategy.h
    include/format.h
    include/Function.h
    include/GenericBands.h
    include/GenericDHStateBands.h
    include/GenericStateBands.h
    include/GreatCircle.h
    include/Horizontal.h
    include/HysteresisData.h
    include/IndexLevelT.h
    include/Integerval.h
    include/Interval.h
    include/IntervalSet.h
    include/Kinematics.h
    include/KinematicsLatLon.h
    include/LatLonAlt.h
    include/LossData.h
    include/MofN.h
    include/NavPoint.h
    include/NoneUrgencyStrategy.h
    include/OrthographicProjection.h
    include/OutputList.h
    include/Pair.h
    include/ParameterAcceptor.h
    include/ParameterData.h
    include/ParameterEntry.h
    include/ParameterProvider.h
    include/ParameterReader.h
    include/ParameterTable.h
    include/Point.h
    include/Position.h
    include/PositionUtil.h
    include/ProjectedKinematics.h
    include/Projection.h
    include/Quad.h
    include/RecoveryInformation.h
    include/SeparatedInput.h
    include/SeparatedOutput.h
    include/SequenceReader.h
    include/SimpleNoPolarProjection.h
    include/SimpleProjection.h
    include/StateReader.h
    include/StateVector.h
    include/string_util.h
    include/SUMData.h
    include/TangentLine.h
    include/TargetUrgency.h
    include/TCAS2D.h
    include/TCAS3D.h
    include/TCASTable.h
    include/TrafficState.h
    include/Transmitter.h
    include/Triple.h
    include/Tuple5.h
    include/Units.h
    include/UrgencyStrategy.h
    include/Util.h
    include/Vect2.h
    include/Vect3.h
    include/VectFuns.h
    include/Velocity.h
    include/Vertical.h
    include/WCV_HZ.h
    include/WCVTable.h
    include/WCV_TAUMOD.h
    include/WCV_TAUMOD_SUM.h
    include/WCV_TCOA.h
    include/WCV_TCPA.h
    include/WCV_TEP.h
    include/WCV_tvar.h
    include/WCV_Vertical.h
    include/WCV_VMOD.h
)

set_target_properties(Daidalus PROPERTIES PUBLIC_HEADER "${HEADERS}")

install(TARGETS Daidalus
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib
        PUBLIC_HEADER DESTINATION include/Daidalus
)

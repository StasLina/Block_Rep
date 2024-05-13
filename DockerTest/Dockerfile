FROM debian:bullseye
RUN apt-get update && apt-get install -y git
ENV LD_LIBRARY_PATH=./Block_Rep/bin
RUN git clone -b Polyhedron_graph_triggers_PostgreSQL http://git.hronos.su:8080/Stanislav_KHoziaenok/Block_Rep.git
ENV MATH_HANDLER_TARGET_PLATFORM="linux"
ENV MATH_HANDLER_LACAL_PATH=./Block_Rep
ENV MATH_HANDLER_SETTING_PATH=./Block_Rep
ENV MATH_HANDLER_EXCEPTION_PATH=./Block_Rep
RUN echo "Heelo"
RUN echo $MATH_HANDLER_TARGET_PLATFORM
RUN echo $MATH_HANDLER_LACAL_PATH
ENTRYPOINT Block_Rep/bin/Block bb_setting-path=/foo bb_local-path=/foo bb_exception-path=/foo/logs path_to_coordinates_of_the_block_shape=/foo

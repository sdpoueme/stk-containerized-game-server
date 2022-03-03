FROM gameserver-debian-base:latest
RUN apt-get install git -y
RUN git clone https://github.com/supertuxkart/stk-code stk-code
RUN cd stk-code
RUN mkdir cmake_build
RUN cmake ../stk-code -B ./cmake_build -DCHECK_ASSETS=off -DSERVER_ONLY=ON
RUN cd cmake_build && make -j$(nproc) -f ./Makefile

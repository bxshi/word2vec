cmake_minimum_required(VERSION 3.3)
project(word2vec)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR})

set(CMAKE_CXX_FLAGE "${CMAKE_CXX_FLATS} -lm -pthread -O3 -march=native -Wall -funroll-loops -Wno-unused-result")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(WORD2VEC_SOURCE word2vec.c)
set(WORD2PHRASE_SOURCE word2phrase.c)
set(DISTANCE_SOURCE distance.c)
set(WORDANALOGY_SOURCE word-analogy.c)
set(ACCURACY_SOURCE compute-accuracy.c)

add_executable(word2vec ${WORD2VEC_SOURCE})
add_executable(word2phrase ${WORD2PHRASE_SOURCE})
add_executable(distance ${DISTANCE_SOURCE})
add_executable(word-analogy ${WORDANALOGY_SOURCE})
add_executable(compute-accuracy ${ACCURACY_SOURCE})
# Copyright (c) Facebook, Inc. and its affiliates.
#
# This source code is licensed under the MIT license found in the
# LICENSE file in the root directory of this source tree.

if(NOT BUILD_TESTS)
  return()
endif()

quic_add_test(TARGET QuicLossFunctionsTest
  SOURCES
  QuicLossFunctionsTest.cpp
  DEPENDS
  Folly::folly
  mvfst_codec_types
  mvfst_client
  mvfst_loss
  mvfst_mock_socket
  mvfst_mock_state
  mvfst_server
  mvfst_test_utils
  mvfst_transport
  ${LIBGTEST_LIBRARY}
)

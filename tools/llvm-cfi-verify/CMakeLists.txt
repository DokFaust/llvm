set(LLVM_LINK_COMPONENTS
  AllTargetsAsmPrinters
  AllTargetsAsmParsers
  AllTargetsDescs
  AllTargetsDisassemblers
  AllTargetsInfos
  MC
  MCParser
  Object
  Support
  Symbolize
  )

add_llvm_tool(llvm-cfi-verify DISABLE_LLVM_LINK_LLVM_DYLIB
  llvm-cfi-verify.cpp)

add_subdirectory(lib)
target_link_libraries(llvm-cfi-verify PRIVATE LLVMCFIVerify)

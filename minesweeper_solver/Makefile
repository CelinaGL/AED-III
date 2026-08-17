ifeq ($(OS),Windows_NT)
    EXT := .exe
    GENERATOR := -G "MinGW Makefiles"
    RUN_PREFIX :=
    MKDIR := if not exist build mkdir build
    RMDIR := if exist build rmdir /s /q build
else
    EXT :=
    GENERATOR :=
    RUN_PREFIX := ./
    MKDIR := mkdir -p build
    RMDIR := rm -rf build
endif

.PHONY: build run clean run-autoplayer run-k-convergence run-scaling run-sensitivity run-calibration run-all
build:
	$(MKDIR)
	cd build && cmake .. $(GENERATOR) && cmake --build .

run: build
	cd build && $(RUN_PREFIX)benchmark$(EXT) && $(RUN_PREFIX)tests$(EXT)

run-autoplayer: build
	cd build && $(RUN_PREFIX)autoplayer$(EXT)

run-k-convergence: build
	cd build && $(RUN_PREFIX)k_convergence$(EXT)

run-scaling: build
	cd build && $(RUN_PREFIX)scaling_curve$(EXT)

run-sensitivity: build
	cd build && $(RUN_PREFIX)sensitivity$(EXT)

run-calibration: build
	cd build && $(RUN_PREFIX)calibration$(EXT)

run-benchmark-mc-vs-bf: build
	cd build && $(RUN_PREFIX)benchmark_mc_vs_bf$(EXT)

run-all: build
	cd build && $(RUN_PREFIX)benchmark$(EXT) && $(RUN_PREFIX)tests$(EXT) && $(RUN_PREFIX)autoplayer$(EXT) && $(RUN_PREFIX)k_convergence$(EXT) && $(RUN_PREFIX)scaling_curve$(EXT) && $(RUN_PREFIX)sensitivity$(EXT) && $(RUN_PREFIX)calibration$(EXT)

clean:
	rm -rf build
# VHDL Process Sensitivity List Issue

This repository demonstrates a common error in VHDL code involving process sensitivity lists. The code in `bad_process.vhdl` exhibits an incorrect process declaration that leads to unexpected behavior.

The `bad_process` entity is meant to pass the input `data_in` to the output `data_out` when a rising edge of the clock signal is detected. However, the process is only sensitive to the clock signal (`clk`).  This means that changes to `data_in` will not immediately be reflected in `data_out`. The correct solution involves making the process sensitive to `data_in` as well.

The solution is provided in `good_process.vhdl`, showing how to correctly specify the process sensitivity list.
# Board installation
In the following the required installation steps for the supported boards

## Nexys, Basys, Arty, Zybo and Zedboard Families
Verified on Vivado 2022.1 (should be working from 2015.1 onward):
   - Download the [Digilent Legacy board files](https://github.com/Digilent/vivado-boards/archive/master.zip)
   - Extract the downloaded zip and copy new/board_files/* into \<VIVADO_DIR>/data/boards/board_files
   - Restart vivado

## Alveo U250
Verified on Vivado 2023.1:
   - Download the [Alveo U250 board files](https://www.xilinx.com/bin/public/openDownload?filename=au250_board_files_20200616.zip)
   - Extract the downloaded zip into \<VIVADO_DIR>/data/xhub/boards/XilinxBoardStore/boards/Xilinx/
   - Restart Vivado
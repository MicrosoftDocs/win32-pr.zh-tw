---
title: 在 RIFF 檔案上執行檔案 i/o
description: 在 RIFF 檔案上執行檔案 i/o
ms.assetid: 3ffc5975-7acb-4844-89b0-bf245b3bd316
keywords:
- 多媒體檔案 i/o、RIFF 檔
- 檔案 i/o，RIFF 檔案
- 輸入和輸出 (i/o) ，RIFF 檔
- I/o (輸入和輸出) 、RIFF 檔
- " (RIFF) 的資源交換檔案格式"
- 'RIFF (資源交換檔案格式) '
- RIFF I/O
- 緩衝的 i/o
- RIFF 區塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5e13fd50d98ea8042bb143c135d839b9b570475
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932103"
---
# <a name="performing-file-io-on-riff-files"></a><span data-ttu-id="d7ce5-112">在 RIFF 檔案上執行檔案 i/o</span><span class="sxs-lookup"><span data-stu-id="d7ce5-112">Performing File I/O on RIFF Files</span></span>

<span data-ttu-id="d7ce5-113">下列範例示範如何針對已緩衝處理的 i/o 開啟 RIFF 檔，以及如何下降、遞增和讀取 "RIFF" 區塊。</span><span class="sxs-lookup"><span data-stu-id="d7ce5-113">The following example shows how to open a RIFF file for buffered I/O, as well as how to descend, ascend, and read "RIFF" chunks.</span></span>


```C++
// ReversePlay--Plays a waveform-audio file backward. 
void ReversePlay() 
{ 
    char        szFileName[128];    // filename of file to open 
    HMMIO       hmmio;              // file handle for open file 
    MMCKINFO    mmckinfoParent;     // parent chunk information 
    MMCKINFO    mmckinfoSubchunk;   // subchunk information structure 
    DWORD       dwFmtSize;          // size of "FMT" chunk 
    DWORD       dwDataSize;         // size of "DATA" chunk 
    WAVEFORMAT  *pFormat;           // address of "FMT" chunk 
    HPSTR       lpData;             // address of "DATA" chunk 
 
    // Get the filename from the edit control. 
    . 
    . 
    . 
    // Open the file for reading with buffered I/O 
    // by using the default internal buffer 
    if(!(hmmio = mmioOpen(szFileName, NULL, 
        MMIO_READ | MMIO_ALLOCBUF))) 
    { 
        Error("Failed to open file."); 
        return; 
    } 
 
    // Locate a "RIFF" chunk with a "WAVE" form type to make 
    // sure the file is a waveform-audio file. 
    mmckinfoParent.fccType = mmioFOURCC('W', 'A', 'V', 'E'); 
    if (mmioDescend(hmmio, (LPMMCKINFO) &mmckinfoParent, NULL, 
        MMIO_FINDRIFF)) 
    { 
        Error("This is not a waveform-audio file."); 
        mmioClose(hmmio, 0); 
        return; 
    } 
    // Find the "FMT" chunk (form type "FMT"); it must be 
    // a subchunk of the "RIFF" chunk. 
    mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
    if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
        MMIO_FINDCHUNK)) 
    { 
        Error("Waveform-audio file has no "FMT" chunk."); 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Get the size of the "FMT" chunk. Allocate 
    // and lock memory for it. 
    dwFmtSize = mmckinfoSubchunk.cksize; 
    . 
    . 
    . 
    // Read the "FMT" chunk. 
    if (mmioRead(hmmio, (HPSTR) pFormat, dwFmtSize) != dwFmtSize){ 
        Error("Failed to read format chunk."); 
        . 
        . 
        . 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Ascend out of the "FMT" subchunk. 
    mmioAscend(hmmio, &mmckinfoSubchunk 0); 
 
    // Find the data subchunk. The current file position should be at 
    // the beginning of the data chunk; however, you should not make 
    // this assumption. Use mmioDescend to locate the data chunk. 
    mmckinfoSubchunk.ckid = mmioFOURCC('d', 'a', 't', 'a'); 
    if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
        MMIO_FINDCHUNK)) 
    { 
        Error("Waveform-audio file has no data chunk."); 
        . 
        . 
        . 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Get the size of the data subchunk. 
    dwDataSize = mmckinfoSubchunk.cksize; 
    if (dwDataSize == 0L){ 
        Error("The data chunk contains no data."); 
        . 
        . 
        . 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Open a waveform-audio output device. 
    . 
    . 
    . 
 
    // Allocate and lock memory for the waveform-audio data. 
    . 
    . 
    . 
 
    // Read the waveform-audio data subchunk. 
    if(mmioRead(hmmio, (HPSTR) lpData, dwDataSize) != dwDataSize){ 
        Error("Failed to read data chunk."); 
        . 
        . 
        . 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Close the file. 
    mmioClose(hmmio, 0); 
 
    // Reverse the sound and play it. 
    . 
    . 
    . 
} 

```



 

 





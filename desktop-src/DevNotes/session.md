---
description: 會話結構包含目前會話的相關資訊。
ms.assetid: e04571f9-eeb7-4612-8cb2-05aca7b5df06
title: 會話結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSION
api_type:
- NA
api_location: ''
ms.openlocfilehash: db283c735e87fb88b489c3ad8367b37ab867c9627fffa7b6052706e0d260b54e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075942"
---
# <a name="session-structure"></a>會話結構

\[只有在使用不支援的 **DeleteExtractedFiles** 和 **解壓縮** 函式時，此結構才會包含所需的資訊。 本檔僅供參考之用。\]

**會話** 結構包含目前會話的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  ACTION    act;
  HFILELIST hflist;
  BOOL      fAllCabinets;
  BOOL      fOverwrite;
  BOOL      fNoLineFeed;
  BOOL      fSelfExtract;
  long      cbSelfExtractSize;
  long      cbSelfExtractSize;
  int       ahfSelf[cMAX_CAB_FILE_OPEN];
  int       cErrors;
  HFDI      hfdi;
  ERF       erf;
  long      cFiles;
  long      cbTotalBytes;
  PERROR    perr;
  SPILLERR  se;
  long      cbSpill;
  char      achSelf[cbFILE_NAME_MAX];
  char      achMsg[cbMAX_LINE*2];
  char      achLine;
  char      achLocation;
  char      achFile;
  char      achDest;
  char      achCabPath;
  BOOL      fContinuationCabinet;
  BOOL      fShowReserveInfo;
  BOOL      fNextCabCalled;
  CABINET   acab[2];
  char      achZap[cbFILE_NAME_MAX];
  char      achCabinetFile[cbFILE_NAME_MAX];
  int       cArgv;
  char      **pArgv;
  int       fDestructive;
  USHORT    iCurrentFolder;
} SESSION, *PSESSION;
```



## <a name="members"></a>成員

<dl> <dt>

**行為**
</dt> <dd>

要執行的動作。 這個成員可以是下列列舉型別中的其中一個值。

``` syntax
typedef enum {
    actBAD,         // Invalid action
    actHELP,        // Show help
    actDEFAULT,     // Perform default action based on command line arguments
    actDIRECTORY,   // Force display of cabinet directory
    actEXTRACT,     // Force file extraction
    actCOPY,        // Do single file-to-file copy
} ACTION;  
```

</dd> <dt>

**hflist**
</dt> <dd>

命令列上所指定檔案清單的控制碼。 這個資料類型的宣告方式如下：

`typedef void *HFILELIST;`

</dd> <dt>

**fAllCabinets**
</dt> <dd>

旗標，指出是否應該處理一個以上的封包檔。 如果這個值為 **TRUE**，則會處理接續封包。

</dd> <dt>

**fOverwrite**
</dt> <dd>

指出是否應該覆寫現有檔案的旗標。 如果這個值為 **TRUE**，則會覆寫現有的檔案。

</dd> <dt>

**fNoLineFeed**
</dt> <dd>

旗標，指出最後一個 `printf` 呼叫是否有分行符號 (`\n`) 個字元。 如果這個值為 **TRUE**，則表示最後一個 `printf` 呼叫未包含分行符號。

</dd> <dt>

**fSelfExtract**
</dt> <dd>

指出封包是否為自我解壓縮的旗標。 如果這個值為 **TRUE**，封包會自我解壓縮。

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

可執行檔 (.exe 的長度) 部分的自動解壓縮封包。

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

自動解壓縮封包的 CAB 部分長度。

</dd> <dt>

**ahfSelf**
</dt> <dd>

封包的檔案控制代碼。

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

**cErrors**
</dt> <dd>

在解壓縮會話期間遇到的錯誤計數。

</dd> <dt>

**hfdi**
</dt> <dd>

FDI 內容的控制碼。 這個資料類型的宣告方式如下：

`typedef void FAR *HFDI; `

</dd> <dt>

**erf**
</dt> <dd>

FDI 錯誤結構。 請參閱 [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)。

</dd> <dt>

**cFiles**
</dt> <dd>

已處理的檔案計數。

</dd> <dt>

**cbTotalBytes**
</dt> <dd>

已解壓縮的位元組總數。

</dd> <dt>

**perr**
</dt> <dd>

傳遞 FDI。

</dd> <dt>

**硒**
</dt> <dd>

溢出檔案錯誤。 這個成員可以是下列列舉型別中的其中一個值。

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

**cbSpill**
</dt> <dd>

要求的溢出檔案大小。

</dd> <dt>

**achSelf**
</dt> <dd>

可執行檔 (.exe) 檔的名稱。

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achMsg**
</dt> <dd>

訊息格式化緩衝區。

`#define cbMAX_LINE          256`

</dd> <dt>

**achLine**
</dt> <dd>

行格式化緩衝區。

</dd> <dt>

**achLocation**
</dt> <dd>

輸出目錄。

</dd> <dt>

**achFile**
</dt> <dd>

目前正在解壓縮的檔案名。

</dd> <dt>

**achDest**
</dt> <dd>

強制的目的地檔案名。

</dd> <dt>

**achCabPath**
</dt> <dd>

要查看封包檔的路徑。

</dd> <dt>

**fContinuationCabinet**
</dt> <dd>

旗標，指出目前的封包是否為第一個已處理的封包。 如果設定為 **TRUE**，則不是第一個處理的封包。

</dd> <dt>

**fShowReserveInfo**
</dt> <dd>

指出是否應提供保留資訊的旗標。 如果設定為 **TRUE**，則會提供資訊。

</dd> <dt>

**fNextCabCalled**
</dt> <dd>

當我們處理封包集中的所有檔案時，這個成員會提供一種方法來判斷要使用哪一個 **acab** 專案 (**FAllCabinet** 設定為 **TRUE**) 。

</dd> <dt>

**acab**
</dt> <dd>

封包集中的最後兩個專案。 此結構的定義如下：

``` syntax
typedef struct {
    char    achCabPath[cbFILE_NAME_MAX];     // Cabinet file path
    char    achCabFilename[cbFILE_NAME_MAX]; // Cabinet file name.ext
    char    achDiskName[cbFILE_NAME_MAX];    // User readable disk label
    USHORT  setID;
    USHORT  iCabinet;
} CABINET;
typedef CABINET *PCABINET;
```

</dd> <dt>

**achZap**
</dt> <dd>

要從檔案名中去除的前置詞。

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achCabinetFile**
</dt> <dd>

目前的封包檔。

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**cArgv**
</dt> <dd>

預設的自我解壓縮 argc。

</dd> <dt>

**pArgv**
</dt> <dd>

指向預設自我解壓縮 argv 之指標的指標 \[ \] 。

</dd> <dt>

**fDestructive**
</dt> <dd>

將設定為 **TRUE** 時所需的磁碟空間最小化的旗標。

</dd> <dt>

**iCurrentFolder**
</dt> <dd>

如果 **fDestructive** 設定為 **TRUE**，則只解壓縮目前的資料夾。

</dd> </dl>

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**擷取**](extract.md)
</dt> </dl>

 

 

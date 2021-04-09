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
ms.openlocfilehash: 9e1f356020df681e00f43c7a47ac16048764c0ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688512"
---
# <a name="session-structure"></a><span data-ttu-id="ba1ad-103">會話結構</span><span class="sxs-lookup"><span data-stu-id="ba1ad-103">SESSION structure</span></span>

<span data-ttu-id="ba1ad-104">\[只有在使用不支援的 **DeleteExtractedFiles** 和 **解壓縮** 函式時，此結構才會包含所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-104">\[This structure contains information required only when using the **DeleteExtractedFiles** and **Extract** functions, which are not supported.</span></span> <span data-ttu-id="ba1ad-105">本檔僅供參考之用。\]</span><span class="sxs-lookup"><span data-stu-id="ba1ad-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="ba1ad-106">**會話** 結構包含目前會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-106">The **SESSION** structure contains information about the current session.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba1ad-107">語法</span><span class="sxs-lookup"><span data-stu-id="ba1ad-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="ba1ad-108">成員</span><span class="sxs-lookup"><span data-stu-id="ba1ad-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba1ad-109">**行為**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-109">**act**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-110">要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-110">The action to perform.</span></span> <span data-ttu-id="ba1ad-111">這個成員可以是下列列舉型別中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-111">This member can be one of the values from the following enumerated type.</span></span>

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

<span data-ttu-id="ba1ad-112">**hflist**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-112">**hflist**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-113">命令列上所指定檔案清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-113">The handle to a list of files specified on the command line.</span></span> <span data-ttu-id="ba1ad-114">這個資料類型的宣告方式如下：</span><span class="sxs-lookup"><span data-stu-id="ba1ad-114">This datatype is declared as follows:</span></span>

`typedef void *HFILELIST;`

</dd> <dt>

<span data-ttu-id="ba1ad-115">**fAllCabinets**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-115">**fAllCabinets**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-116">旗標，指出是否應該處理一個以上的封包檔。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-116">A flag that indicates whether more than one cabinet file should be processed.</span></span> <span data-ttu-id="ba1ad-117">如果這個值為 **TRUE**，則會處理接續封包。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-117">If this value is **TRUE**, continuation cabinets are processed.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-118">**fOverwrite**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-118">**fOverwrite**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-119">指出是否應該覆寫現有檔案的旗標。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-119">A flag that indicates whether existing files should be overwritten.</span></span> <span data-ttu-id="ba1ad-120">如果這個值為 **TRUE**，則會覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-120">If this value is **TRUE**, existing files are overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-121">**fNoLineFeed**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-121">**fNoLineFeed**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-122">旗標，指出最後一個 `printf` 呼叫是否有分行符號 (`\n`) 個字元。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-122">A flag that indicates whether the last `printf` call has the newline (`\n`) characters.</span></span> <span data-ttu-id="ba1ad-123">如果這個值為 **TRUE**，則表示最後一個 `printf` 呼叫未包含分行符號。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-123">If this value is **TRUE**, the last `printf` call did not include the newline characters.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-124">**fSelfExtract**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-124">**fSelfExtract**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-125">指出封包是否為自我解壓縮的旗標。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-125">A flag that indicates whether a cabinet is self extracting.</span></span> <span data-ttu-id="ba1ad-126">如果這個值為 **TRUE**，封包會自我解壓縮。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-126">If this value is **TRUE**, the cabinet is self extracting.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-127">**cbSelfExtractSize**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-127">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-128">可執行檔 ( .exe 的長度) 部分的自動解壓縮封包。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-128">The length of the executable (.exe) portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-129">**cbSelfExtractSize**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-129">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-130">自動解壓縮封包的 CAB 部分長度。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-130">The length of the CAB portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-131">**ahfSelf**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-131">**ahfSelf**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-132">封包的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-132">The file handles to the cabinet.</span></span>

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

<span data-ttu-id="ba1ad-133">**cErrors**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-133">**cErrors**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-134">在解壓縮會話期間遇到的錯誤計數。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-134">The count of errors encountered during the extraction session.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-135">**hfdi**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-135">**hfdi**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-136">FDI 內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-136">A handle to the FDI context.</span></span> <span data-ttu-id="ba1ad-137">這個資料類型的宣告方式如下：</span><span class="sxs-lookup"><span data-stu-id="ba1ad-137">This datatype is declared as follows:</span></span>

`typedef void FAR *HFDI; `

</dd> <dt>

<span data-ttu-id="ba1ad-138">**erf**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-138">**erf**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-139">FDI 錯誤結構。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-139">The FDI error structure.</span></span> <span data-ttu-id="ba1ad-140">請參閱 [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-140">See [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-141">**cFiles**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-141">**cFiles**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-142">已處理的檔案計數。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-142">The count of files processed.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-143">**cbTotalBytes**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-143">**cbTotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-144">已解壓縮的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-144">The total number of bytes extracted.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-145">**perr**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-145">**perr**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-146">傳遞 FDI。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-146">The pass through FDI.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-147">**硒**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-147">**se**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-148">溢出檔案錯誤。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-148">The spill file error.</span></span> <span data-ttu-id="ba1ad-149">這個成員可以是下列列舉型別中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-149">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

<span data-ttu-id="ba1ad-150">**cbSpill**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-150">**cbSpill**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-151">要求的溢出檔案大小。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-151">The size of the spill file requested.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-152">**achSelf**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-152">**achSelf**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-153">可執行檔 ( .exe) 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-153">The name of the executable (.exe) file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="ba1ad-154">**achMsg**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-154">**achMsg**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-155">訊息格式化緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-155">The message formatting buffer.</span></span>

`#define cbMAX_LINE          256`

</dd> <dt>

<span data-ttu-id="ba1ad-156">**achLine**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-156">**achLine**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-157">行格式化緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-157">The line formatting buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-158">**achLocation**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-158">**achLocation**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-159">輸出目錄。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-159">The output directory.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-160">**achFile**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-160">**achFile**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-161">目前正在解壓縮的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-161">The current file name being extracted.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-162">**achDest**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-162">**achDest**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-163">強制的目的地檔案名。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-163">The forced destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-164">**achCabPath**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-164">**achCabPath**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-165">要查看封包檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-165">The path to look at for a cabinet file.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-166">**fContinuationCabinet**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-166">**fContinuationCabinet**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-167">旗標，指出目前的封包是否為第一個已處理的封包。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-167">A flag that indicates whether the current cabinet is the first one processed.</span></span> <span data-ttu-id="ba1ad-168">如果設定為 **TRUE**，則不是第一個處理的封包。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-168">If set to **TRUE**, it is not the first cabinet processed.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-169">**fShowReserveInfo**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-169">**fShowReserveInfo**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-170">指出是否應提供保留資訊的旗標。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-170">A flag that indicates whether reserve information should be provided.</span></span> <span data-ttu-id="ba1ad-171">如果設定為 **TRUE**，則會提供資訊。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-171">If set to **TRUE**, the information is made available.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-172">**fNextCabCalled**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-172">**fNextCabCalled**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-173">當我們處理封包集中的所有檔案時，這個成員會提供一種方法來判斷要使用哪一個 **acab** 專案 (**FAllCabinet** 設定為 **TRUE**) 。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-173">This member provides a way to determine which of the **acab** entries to use if we are processing all files in a cabinet set (**fAllCabinet** is set to **TRUE**).</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-174">**acab**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-174">**acab**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-175">封包集中的最後兩個專案。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-175">The last two entries in the cabinet set.</span></span> <span data-ttu-id="ba1ad-176">此結構的定義如下：</span><span class="sxs-lookup"><span data-stu-id="ba1ad-176">This structure is defined as follows:</span></span>

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

<span data-ttu-id="ba1ad-177">**achZap**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-177">**achZap**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-178">要從檔案名中去除的前置詞。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-178">The prefix to strip from the file name.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="ba1ad-179">**achCabinetFile**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-179">**achCabinetFile**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-180">目前的封包檔。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-180">The current cabinet file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="ba1ad-181">**cArgv**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-181">**cArgv**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-182">預設的自我解壓縮 argc。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-182">The default self-extracting argc.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-183">**pArgv**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-183">**pArgv**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-184">指向預設自我解壓縮 argv 之指標的指標 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-184">A pointer to a pointer to the default self-extracting argv\[\].</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-185">**fDestructive**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-185">**fDestructive**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-186">將設定為 **TRUE** 時所需的磁碟空間最小化的旗標。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-186">A flag that minimizes the disk space needed when set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="ba1ad-187">**iCurrentFolder**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-187">**iCurrentFolder**</span></span>
</dt> <dd>

<span data-ttu-id="ba1ad-188">如果 **fDestructive** 設定為 **TRUE**，則只解壓縮目前的資料夾。</span><span class="sxs-lookup"><span data-stu-id="ba1ad-188">If **fDestructive** is set to **TRUE**, extract only the current folder.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="ba1ad-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba1ad-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba1ad-190">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-190">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="ba1ad-191">**提取**</span><span class="sxs-lookup"><span data-stu-id="ba1ad-191">**Extract**</span></span>](extract.md)
</dt> </dl>

 

 

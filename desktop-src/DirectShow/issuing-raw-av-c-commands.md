---
description: 發出原始的 AV/C 命令
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: 發出原始的 AV/C 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385651"
---
# <a name="issuing-raw-avc-commands"></a><span data-ttu-id="d78ac-103">發出原始的 AV/C 命令</span><span class="sxs-lookup"><span data-stu-id="d78ac-103">Issuing Raw AV/C Commands</span></span>

<span data-ttu-id="d78ac-104">[**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)、 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)和 [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader)介面的運作方式是將方法呼叫轉譯為驅動程式的命令，然後解讀驅動程式的回應，並透過 **HRESULT** 或 output 參數傳回該驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d78ac-104">The [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport), and [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) interfaces work by translating the method calls into commands for the driver, then interpreting the driver's response and returning it through an **HRESULT** or an output parameter.</span></span> <span data-ttu-id="d78ac-105">不過，某些裝置功能可能無法透過這些方法存取。</span><span class="sxs-lookup"><span data-stu-id="d78ac-105">However, some device functions may not be accessible through these methods.</span></span> <span data-ttu-id="d78ac-106">因此，MSDV 支援將原始的 AV/C 命令傳送到裝置。</span><span class="sxs-lookup"><span data-stu-id="d78ac-106">Therefore, MSDV supports sending raw AV/C commands to the device.</span></span>

<span data-ttu-id="d78ac-107">使用這項功能時，您應該記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="d78ac-107">You should keep the following points in mind when using this feature:</span></span>

-   <span data-ttu-id="d78ac-108">此命令會直接傳遞至裝置，而不會進行錯誤檢查或參數驗證。</span><span class="sxs-lookup"><span data-stu-id="d78ac-108">The command is passed directly to the device, with no error checking or parameter validation.</span></span> <span data-ttu-id="d78ac-109">基於這個理由，只有當 DirectShow 介面未執行您所需的功能時，您才應該發出原始的 AV/C 命令。</span><span class="sxs-lookup"><span data-stu-id="d78ac-109">For this reason, you should issue raw AV/C commands only when the DirectShow interfaces do not implement the functionality you need.</span></span>
-   <span data-ttu-id="d78ac-110">所有原始的 AV/C 命令都是同步的。</span><span class="sxs-lookup"><span data-stu-id="d78ac-110">All raw AV/C commands are synchronous.</span></span> <span data-ttu-id="d78ac-111">發出命令的執行緒會封鎖，直到命令返回為止。</span><span class="sxs-lookup"><span data-stu-id="d78ac-111">The thread issuing the command blocks until the command returns.</span></span>
-   <span data-ttu-id="d78ac-112">一次只能指定一個命令。</span><span class="sxs-lookup"><span data-stu-id="d78ac-112">Only one command can be given at a time.</span></span> <span data-ttu-id="d78ac-113">處理此命令時，裝置將會拒絕任何其他命令。</span><span class="sxs-lookup"><span data-stu-id="d78ac-113">While the command is being processed, the device will reject any additional commands.</span></span>
-   <span data-ttu-id="d78ac-114">UVC 驅動程式不支援原始的 AV/C 命令。</span><span class="sxs-lookup"><span data-stu-id="d78ac-114">The UVC driver does not support raw AV/C commands.</span></span>

<span data-ttu-id="d78ac-115">若要傳送 AV/C 命令，請將命令格式化為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="d78ac-115">To send an AV/C command, format the command as an array of bytes.</span></span> <span data-ttu-id="d78ac-116">然後呼叫 [**IAMExtTransport：： GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters)。</span><span class="sxs-lookup"><span data-stu-id="d78ac-116">Then call [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span></span> <span data-ttu-id="d78ac-117">傳入 ED \_ RAW \_ EXT \_ DEV \_ CMD 旗標、陣列大小，以及陣列。</span><span class="sxs-lookup"><span data-stu-id="d78ac-117">Pass in the ED\_RAW\_EXT\_DEV\_CMD flag, the array size, and the array.</span></span> <span data-ttu-id="d78ac-118">因為此參數的原始用途是要傳回字串值，所以您必須將陣列位址轉換成 \**LPOLESTR \** _ 類型。</span><span class="sxs-lookup"><span data-stu-id="d78ac-118">You must cast the array address to an \**LPOLESTR\** _ type, because the original purpose of this parameter was to return a string value.</span></span>


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR_) AvcCmd);
```



<span data-ttu-id="d78ac-119">陣列的內容會直接傳遞至裝置，因此您必須小心正確地將它格式化。</span><span class="sxs-lookup"><span data-stu-id="d78ac-119">The contents of the array are passed directly to the device, so you must be careful to format it correctly.</span></span> <span data-ttu-id="d78ac-120">命令可以將裝置的目標設為 (的) 或 (磁帶或相機) 的子單位。</span><span class="sxs-lookup"><span data-stu-id="d78ac-120">A command can target the unit (camcorder) or a subunit (tape or camera).</span></span> <span data-ttu-id="d78ac-121">您可以從 [1394 貿易協會網站](https://1394ta.org)取得相關標準。</span><span class="sxs-lookup"><span data-stu-id="d78ac-121">The relevant standards are available from the [1394 Trade Association Web site](https://1394ta.org).</span></span>

-   <span data-ttu-id="d78ac-122">AV/C 數位介面命令集一般規格</span><span class="sxs-lookup"><span data-stu-id="d78ac-122">AV/C Digital Interface Command Set General Specification</span></span>
-   <span data-ttu-id="d78ac-123">AV/C 磁帶錄製器/播放機子單位規格</span><span class="sxs-lookup"><span data-stu-id="d78ac-123">AV/C Tape Recorder/Player Subunit Specification</span></span>

<span data-ttu-id="d78ac-124">先前的說明如何格式化 AV/C 命令，並列出單位命令。</span><span class="sxs-lookup"><span data-stu-id="d78ac-124">The former describes how to format AV/C commands and lists the unit commands.</span></span> <span data-ttu-id="d78ac-125">後者的規格會列出次級命令。</span><span class="sxs-lookup"><span data-stu-id="d78ac-125">The latter specification lists the subunit commands.</span></span>

<span data-ttu-id="d78ac-126">**GetTransportBasicParameters** 方法可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="d78ac-126">The **GetTransportBasicParameters** method may return one of the following error codes:</span></span>



| <span data-ttu-id="d78ac-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d78ac-127">Error Code</span></span>              | <span data-ttu-id="d78ac-128">描述</span><span class="sxs-lookup"><span data-stu-id="d78ac-128">Description</span></span>                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d78ac-129">錯誤 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="d78ac-129">ERROR\_TIMEOUT</span></span>          | <span data-ttu-id="d78ac-130">命令逾時。</span><span class="sxs-lookup"><span data-stu-id="d78ac-130">The command timed out.</span></span>                                                           |
| <span data-ttu-id="d78ac-131">錯誤 \_ 需求 \_ 未 \_ ACCEP</span><span class="sxs-lookup"><span data-stu-id="d78ac-131">ERROR\_REQ\_NOT\_ACCEP</span></span>  | <span data-ttu-id="d78ac-132">裝置未接受命令。</span><span class="sxs-lookup"><span data-stu-id="d78ac-132">The device did not accept the command.</span></span>                                           |
| <span data-ttu-id="d78ac-133">\_不 \_ 支援的錯誤</span><span class="sxs-lookup"><span data-stu-id="d78ac-133">ERROR\_NOT\_SUPPORTED</span></span>   | <span data-ttu-id="d78ac-134">裝置不支援此命令。</span><span class="sxs-lookup"><span data-stu-id="d78ac-134">The device does not support the command.</span></span>                                         |
| <span data-ttu-id="d78ac-135">錯誤 \_ 要求已 \_ 中止</span><span class="sxs-lookup"><span data-stu-id="d78ac-135">ERROR\_REQUEST\_ABORTED</span></span> | <span data-ttu-id="d78ac-136">命令已中止。</span><span class="sxs-lookup"><span data-stu-id="d78ac-136">The command was aborted.</span></span> <span data-ttu-id="d78ac-137">Possbly 裝置已移除或發生匯流排重設。</span><span class="sxs-lookup"><span data-stu-id="d78ac-137">Possbly the device was removed or a bus reset occurred.</span></span> |



 

> [!Note]  
> <span data-ttu-id="d78ac-138">這些錯誤會以 Win32 錯誤碼（而非 Hresult）的形式傳回，因此您應該直接測試這些值，而不是使用 **SUCCEEDED** 和 **FAILED** 宏。</span><span class="sxs-lookup"><span data-stu-id="d78ac-138">These errors are returned as Win32 error codes, not HRESULTs, so you should test for these values directly, rather than using the **SUCCEEDED** and **FAILED** macros.</span></span>

 

<span data-ttu-id="d78ac-139">如果方法傳回 S \_ OK，則會將裝置的回應複製到陣列中。</span><span class="sxs-lookup"><span data-stu-id="d78ac-139">If the method returns S\_OK, the response from the device is copied into the array.</span></span> <span data-ttu-id="d78ac-140">回應承載可能會比命令更大，因此您必須配置夠大的緩衝區來保存它。</span><span class="sxs-lookup"><span data-stu-id="d78ac-140">The response payload might be larger than the command, so you must allocate a buffer large enough to hold it.</span></span> <span data-ttu-id="d78ac-141">承載大小上限為512個位元組。</span><span class="sxs-lookup"><span data-stu-id="d78ac-141">The maximum payload size is 512 bytes.</span></span> <span data-ttu-id="d78ac-142">請注意， \_ [確定] 的傳回值不一定表示裝置已成功執行命令。</span><span class="sxs-lookup"><span data-stu-id="d78ac-142">Note that a return value of S\_OK does not always mean the device successfully carried out the command.</span></span> <span data-ttu-id="d78ac-143">應用程式必須檢查回應承載以判斷狀態。</span><span class="sxs-lookup"><span data-stu-id="d78ac-143">The application must examine the response payload to determine the status.</span></span>

<span data-ttu-id="d78ac-144">下列範例顯示用來搜尋絕對曲目編號搜尋的命令：</span><span class="sxs-lookup"><span data-stu-id="d78ac-144">The following example shows the command to search for an absolute track number search:</span></span>


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a><span data-ttu-id="d78ac-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="d78ac-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d78ac-146">控制 DV 攝像機</span><span class="sxs-lookup"><span data-stu-id="d78ac-146">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




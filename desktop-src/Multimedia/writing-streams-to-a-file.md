---
title: 將資料流程寫入檔案
description: 將資料流程寫入檔案
ms.assetid: a3766f8c-aaa6-4fc5-a306-54aee71018f1
keywords:
- AVIFileCreateStream 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370df08534bbdde870f6d28c828d47935abd80db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681918"
---
# <a name="writing-streams-to-a-file"></a><span data-ttu-id="105a1-104">將資料流程寫入檔案</span><span class="sxs-lookup"><span data-stu-id="105a1-104">Writing Streams to a File</span></span>

<span data-ttu-id="105a1-105">您也可以藉由將新的資料流程寫入檔案，來建立包含資料流程的檔案。</span><span class="sxs-lookup"><span data-stu-id="105a1-105">You can also create a file containing data streams by writing a new data stream to a file.</span></span>

<span data-ttu-id="105a1-106">您可以使用 [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) 函數，在新的或現有的檔案中建立新的資料流程。</span><span class="sxs-lookup"><span data-stu-id="105a1-106">You can create a new stream in a new or existing file by using the [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) function.</span></span> <span data-ttu-id="105a1-107">此函式會根據 [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) 結構中所述的特性來定義新的資料流程、建立新資料流程的資料流程介面、遞增資料流程的參考計數，以及傳回資料流程介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="105a1-107">This function defines a new stream according to the characteristics described in an [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) structure, creates a stream interface for the new stream, increments the reference count of the stream, and returns the address of the stream-interface pointer.</span></span>

<span data-ttu-id="105a1-108">寫入資料流程的內容之前，您必須指定資料流程格式。</span><span class="sxs-lookup"><span data-stu-id="105a1-108">Before you write the content of the stream, you must specify the stream format.</span></span> <span data-ttu-id="105a1-109">您可以使用 [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) 函數來設定資料流程格式。</span><span class="sxs-lookup"><span data-stu-id="105a1-109">You can set the stream format by using the [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) function.</span></span> <span data-ttu-id="105a1-110">設定影片資料流程的格式時，您必須以包含適當資訊的 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構提供此函數。</span><span class="sxs-lookup"><span data-stu-id="105a1-110">When setting the format of a video stream, you must supply this function with a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the appropriate information.</span></span> <span data-ttu-id="105a1-111">設定音訊資料流程的格式時，您必須提供 [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) 或 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) 結構，其中包含適當的資訊。</span><span class="sxs-lookup"><span data-stu-id="105a1-111">When setting the format of an audio stream, you must supply a [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) or [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure containing the appropriate information.</span></span> <span data-ttu-id="105a1-112">您需要提供給其他資料流程類型之函式的資訊取決於資料流程類型和資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="105a1-112">The information you need to supply to the function for other stream types depends on the stream type and the stream handler.</span></span>

<span data-ttu-id="105a1-113">您可以使用 [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite) 函式來寫入資料流程中的多媒體內容。</span><span class="sxs-lookup"><span data-stu-id="105a1-113">You can write the multimedia content in a stream by using the [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite) function.</span></span> <span data-ttu-id="105a1-114">此函數會將原始資料從應用程式提供的緩衝區複製到指定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="105a1-114">This function copies raw data from an application-supplied buffer into the specified stream.</span></span> <span data-ttu-id="105a1-115">預設的 AVI 檔處理常式會將資訊附加到資料流程的結尾。</span><span class="sxs-lookup"><span data-stu-id="105a1-115">The default AVI file handler appends information to the end of a stream.</span></span> <span data-ttu-id="105a1-116">預設 WAVE 處理常式可以在資料流程中以及在資料流程的結尾寫入波形音訊資料。</span><span class="sxs-lookup"><span data-stu-id="105a1-116">The default WAVE handler can write waveform-audio data within a stream as well as at the end of a stream.</span></span>

<span data-ttu-id="105a1-117">您可以使用 [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)和 [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)函式，來寫入未包含在 [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)或 [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)函式中之檔案或資料流程的補充資訊。</span><span class="sxs-lookup"><span data-stu-id="105a1-117">You can write supplementary information about the file or stream that is not included in the [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) or [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) function by using the [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) and [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata) functions.</span></span> <span data-ttu-id="105a1-118">您可以使用 **AVIFileWriteData** 來記錄適用于整個檔案的資料，例如著作權資訊和修改歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="105a1-118">You can record data that is applicable to the entire file, such as copyright information and modification history, by using **AVIFileWriteData**.</span></span> <span data-ttu-id="105a1-119">您可以使用 **AVIStreamWriteData** 來記錄資料流程特定的資訊，例如壓縮和解壓縮設定。</span><span class="sxs-lookup"><span data-stu-id="105a1-119">You can record stream-specific information, such as compression and decompression settings, by using **AVIStreamWriteData**.</span></span> <span data-ttu-id="105a1-120">補充資訊儲存在檔案中的不同區塊。</span><span class="sxs-lookup"><span data-stu-id="105a1-120">The supplementary information is stored in separate chunks within the file.</span></span>

<span data-ttu-id="105a1-121">當您使用 [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) 函式完成寫入至新的資料流程之後，就可以關閉資料流程。</span><span class="sxs-lookup"><span data-stu-id="105a1-121">You can close the stream after you finish writing to the new stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="105a1-122">此函式會清除用來記錄資料流程資料的緩衝區，並在檔案中完成並關閉任何不完整的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="105a1-122">This function clears buffers used in recording the stream data, and it completes and closes any incomplete data chunks in the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="105a1-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="105a1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="105a1-124">資料流作業</span><span class="sxs-lookup"><span data-stu-id="105a1-124">Stream Operations</span></span>](stream-operations.md)
</dt> </dl>

 

 
---
title: 影片和音訊區塊細微性
description: 影片和音訊區塊細微性
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- AVI 檔案，區塊細微性
- AVICap 類別，填充區
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932329"
---
# <a name="video-and-audio-chunk-granularity"></a><span data-ttu-id="39169-109">影片和音訊區塊細微性</span><span class="sxs-lookup"><span data-stu-id="39169-109">Video and Audio Chunk Granularity</span></span>

<span data-ttu-id="39169-110">區塊資料細微性是 AVI 檔案的邏輯區塊大小，用於寫入和取出音訊和影片資料區塊。</span><span class="sxs-lookup"><span data-stu-id="39169-110">The chunk granularity is a logical block size for an AVI file that is used for writing and retrieving audio and video data chunks.</span></span> <span data-ttu-id="39169-111">將音訊和影片區塊寫入磁片時，AVICap 會在必要時新增 (RIFF 「垃圾」) 區塊的填充區塊，以填滿每個資料的邏輯區塊。</span><span class="sxs-lookup"><span data-stu-id="39169-111">When writing audio and video chunks to disk, AVICap adds filler chunks (RIFF "JUNK" chunks) as necessary to fill each logical block of data.</span></span>

<span data-ttu-id="39169-112">您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得目前的區塊細微性設定。</span><span class="sxs-lookup"><span data-stu-id="39169-112">You can retrieve the current chunk granularity setting by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="39169-113">目前的區塊資料細微性會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **wChunkGranularity** 成員中。</span><span class="sxs-lookup"><span data-stu-id="39169-113">The current chunk granularity is stored in the **wChunkGranularity** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="39169-114">您可以指定新的區塊資料細微性作為 **wChunkGranularity** 的值，然後使用 [ [**WM \_ CAP \_ SET \_ SEQUENCE \_ 設定**](wm-cap-set-sequence-setup.md)訊息 (] 或 [ [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)宏) ，將更新的 **CAPTUREPARMS** 結構傳送至 [捕獲] 視窗。</span><span class="sxs-lookup"><span data-stu-id="39169-114">You can specify a new chunk granularity as the value of **wChunkGranularity** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="39169-115">您也可以為此成員指定零，將區塊細微性設定為磁片的磁區大小。</span><span class="sxs-lookup"><span data-stu-id="39169-115">You can also specify zero for this member to set the chunk granularity to the sector size of the disk.</span></span>

 

 





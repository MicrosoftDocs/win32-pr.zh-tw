---
title: 寫入變數位元速率資料流程
description: 寫入變數位元速率資料流程
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Advanced Systems Format (ASF) ，撰寫 VBR 資料流程
- ASF (Advanced Systems Format) ，撰寫 VBR 資料流程
- 變數位元速率 (VBR) ，寫入資料流程
- VBR (變數位速率) ，寫入資料流程
- 資料流程，撰寫 VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681382"
---
# <a name="writing-variable-bit-rate-streams"></a><span data-ttu-id="1138c-108">寫入變數位元速率資料流程</span><span class="sxs-lookup"><span data-stu-id="1138c-108">Writing Variable Bit Rate Streams</span></span>

<span data-ttu-id="1138c-109">變數位元速率 (VBR) 資料流程的寫入方式與 (CBR) 資料流程的常數位元速率相同。</span><span class="sxs-lookup"><span data-stu-id="1138c-109">Variable bit rate (VBR) streams are written the same way as constant bit rate (CBR) streams.</span></span> <span data-ttu-id="1138c-110">唯一的差異在於寫入器和編解碼器內部執行的處理。</span><span class="sxs-lookup"><span data-stu-id="1138c-110">The only difference is in the processing performed internally by the writer and the codecs.</span></span> <span data-ttu-id="1138c-111">不過，以位速率為基礎的 VBR (限制和不受限制的) 都需要在寫入器中進行前置處理。</span><span class="sxs-lookup"><span data-stu-id="1138c-111">However, bit rate based VBR (both constrained and unconstrained) requires a preprocessing pass in the writer.</span></span>

<span data-ttu-id="1138c-112">您應該針對每個資料流程，檢查您對 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) 進行第一個呼叫的傳回值。</span><span class="sxs-lookup"><span data-stu-id="1138c-112">You should check the return value for the first call you make to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) for each stream.</span></span> <span data-ttu-id="1138c-113">如果傳回的錯誤碼是 NS \_ E \_ 不正確 \_ NUM \_ pass，則資料流程需要前置處理階段。</span><span class="sxs-lookup"><span data-stu-id="1138c-113">If the error code returned is NS\_E\_INVALID\_NUM\_PASSES, the stream requires a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1138c-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="1138c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1138c-115">**使用 Two-Pass 編碼**</span><span class="sxs-lookup"><span data-stu-id="1138c-115">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="1138c-116">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="1138c-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 





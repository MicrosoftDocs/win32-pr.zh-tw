---
title: 測量視頻品質
description: 測量視頻品質
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021374"
---
# <a name="measuring-video-quality"></a><span data-ttu-id="be1a1-107">測量視頻品質</span><span class="sxs-lookup"><span data-stu-id="be1a1-107">Measuring Video Quality</span></span>

<span data-ttu-id="be1a1-108">測量視頻品質的其中一種方式是限制在捕獲作業期間卸載的已捨棄框架數目。</span><span class="sxs-lookup"><span data-stu-id="be1a1-108">One way to measure video quality is to limit the number of captured frames dropped during the capture operation.</span></span> <span data-ttu-id="be1a1-109">串流處理捕獲完成時，會將品質值與卸載的框架比例與總畫面格的比率進行比較。</span><span class="sxs-lookup"><span data-stu-id="be1a1-109">When streaming capture has finished, the quality value is compared with the ratio of dropped frames to total frames.</span></span> <span data-ttu-id="be1a1-110">如果捨棄的框架百分比大於 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **wPercentDropForError** 成員值，AVICap 會將錯誤訊息傳送至錯誤回呼函式（如果已安裝）。</span><span class="sxs-lookup"><span data-stu-id="be1a1-110">If the percentage of dropped frames is greater than the value of the **wPercentDropForError** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure, AVICap sends an error message to the error callback function if it is installed.</span></span>

<span data-ttu-id="be1a1-111">您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息] (或 [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得目前已卸載框架的限制 (以百分比) 表示。</span><span class="sxs-lookup"><span data-stu-id="be1a1-111">You can retrieve the current limit of dropped frames (expressed as a percentage) by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="be1a1-112">您可以設定新的限制，方法是將百分比指定為 **CAPTUREPARMS** 結構的 **wPercentDropForError** 成員值，然後使用 [ [**WM \_ CAP \_ set \_ SEQUENCE 設定 \_**](wm-cap-set-sequence-setup.md)訊息 (] 或 [ [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)宏) ，將更新的結構傳送至 [捕獲] 視窗。</span><span class="sxs-lookup"><span data-stu-id="be1a1-112">You can set a new limit by specifying a percentage as the value of the **wPercentDropForError** member of the **CAPTUREPARMS** structure, and then sending the updated structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="be1a1-113">**WPercentDropForError** 的預設值為10%。</span><span class="sxs-lookup"><span data-stu-id="be1a1-113">The default value of **wPercentDropForError** is 10 percent.</span></span>

 

 





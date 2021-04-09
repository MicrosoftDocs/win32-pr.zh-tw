---
title: 影片緩衝區
description: 影片緩衝區
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e2f3e5b56f995e6a09792260ac2fd6e1ba5cd7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674588"
---
# <a name="video-buffers"></a><span data-ttu-id="23aba-107">影片緩衝區</span><span class="sxs-lookup"><span data-stu-id="23aba-107">Video Buffers</span></span>

<span data-ttu-id="23aba-108">搭配影片捕獲使用的緩衝區位於記憶體堆積中。</span><span class="sxs-lookup"><span data-stu-id="23aba-108">The buffers used with video capture reside in the memory heap.</span></span> <span data-ttu-id="23aba-109">捕捉作業中所使用的緩衝區數目可能會不同，而且取決於 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **wNumVideoRequested** 成員和可用系統記憶體的值。</span><span class="sxs-lookup"><span data-stu-id="23aba-109">The number of buffers used in a capture operation can vary and depend on the value of the **wNumVideoRequested** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure and available system memory.</span></span>

<span data-ttu-id="23aba-110">您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來抓取要求的視訊緩衝區目前的值。</span><span class="sxs-lookup"><span data-stu-id="23aba-110">You can retrieve the current value of requested video buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="23aba-111">目前要求的影片緩衝區數目會儲存在 **CAPTUREPARMS** 結構的 **wNumVideoRequested** 成員中。</span><span class="sxs-lookup"><span data-stu-id="23aba-111">The current requested number of video buffers is stored in the **wNumVideoRequested** member of the **CAPTUREPARMS** structure.</span></span> <span data-ttu-id="23aba-112">您可以藉由更新這個成員來要求緩衝區的位置和數目，然後使用 [ [**WM \_ CAP \_ SET \_ SEQUENCE 設定 \_**](wm-cap-set-sequence-setup.md)訊息 (] 或 [ [**CapCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)宏) ，將更新的 **CAPTUREPARMS** 結構傳送至 [捕獲] 視窗。</span><span class="sxs-lookup"><span data-stu-id="23aba-112">You can request the placement and number of buffers by updating this member, and then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

 

 





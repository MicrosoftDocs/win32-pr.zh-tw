---
title: User-Initiated Capture
description: User-Initiated Capture
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840508"
---
# <a name="user-initiated-capture"></a><span data-ttu-id="c9fc7-105">User-Initiated Capture</span><span class="sxs-lookup"><span data-stu-id="c9fc7-105">User-Initiated Capture</span></span>

<span data-ttu-id="c9fc7-106">您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得使用者起始之捕獲旗標的目前值。</span><span class="sxs-lookup"><span data-stu-id="c9fc7-106">You can retrieve the current value of the user-initiated capture flag by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="c9fc7-107">旗標的值會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **fMakeUserHitOKToCapture** 成員中。</span><span class="sxs-lookup"><span data-stu-id="c9fc7-107">The value of the flag is stored in the **fMakeUserHitOKToCapture** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="c9fc7-108">您可以藉由將這個成員設定為 **TRUE**，讓使用者精確控制開始抓取會話的時間。</span><span class="sxs-lookup"><span data-stu-id="c9fc7-108">You can provide the user with precise control over when to start a capture session by setting this member to **TRUE**.</span></span> <span data-ttu-id="c9fc7-109">AVICap 會在配置 capture 會話的所有影片和音訊緩衝區之後顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c9fc7-109">AVICap displays a dialog box after allocating all video and audio buffers for a capture session.</span></span> <span data-ttu-id="c9fc7-110">這可讓使用者因軟體初始化而排除捕獲延遲。</span><span class="sxs-lookup"><span data-stu-id="c9fc7-110">This lets the user eliminate capture delays because of software initialization.</span></span> <span data-ttu-id="c9fc7-111">如果您的應用程式使用少量的影片緩衝區，則可能不需要這個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c9fc7-111">If your application uses a small number of video buffers, this dialog box is probably unnecessary.</span></span> <span data-ttu-id="c9fc7-112">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c9fc7-112">The default value is **FALSE**.</span></span>

 

 





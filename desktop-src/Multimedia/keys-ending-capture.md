---
title: 金鑰結束捕獲
description: 金鑰結束捕獲
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- CAPTUREPARMS 結構
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a91d6ee7d07ed36c11cce7e888c9a9710f403cf9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681811"
---
# <a name="keys-ending-capture"></a><span data-ttu-id="4c5c7-108">金鑰結束捕獲</span><span class="sxs-lookup"><span data-stu-id="4c5c7-108">Keys Ending Capture</span></span>

<span data-ttu-id="4c5c7-109">您可以允許使用者在鍵盤上按下按鍵或按鍵組合，或按滑鼠右鍵或滑鼠左鍵，以中止捕捉會話。</span><span class="sxs-lookup"><span data-stu-id="4c5c7-109">You can allow the user to abort a capture session by pressing a key or keystroke combination from the keyboard, or by pressing the right or left mouse button.</span></span> <span data-ttu-id="4c5c7-110">如果使用者中止即時捕獲會話，則會捨棄 capture 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="4c5c7-110">If the user aborts a real-time capture session, the contents of the capture file are discarded.</span></span> <span data-ttu-id="4c5c7-111">如果使用者中止步驟框架捕獲會話，則會儲存捕捉檔案的內容，直到中止捕獲為止。</span><span class="sxs-lookup"><span data-stu-id="4c5c7-111">If the user aborts a step-frame capture session, the contents of the capture file up to the point of aborting the capture are saved.</span></span>

<span data-ttu-id="4c5c7-112">您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得中止捕捉會話的設定。</span><span class="sxs-lookup"><span data-stu-id="4c5c7-112">You can retrieve the settings for aborting a capture session by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="4c5c7-113">目前的按鍵設定會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **vKeyAbort** 成員中;目前的滑鼠設定會儲存在 **fAbortLeftMouse** 和 **fAbortRightMouse** 成員中。</span><span class="sxs-lookup"><span data-stu-id="4c5c7-113">The current keystroke setting is stored in the **vKeyAbort** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure; the current mouse settings are stored in the **fAbortLeftMouse** and **fAbortRightMouse** members.</span></span> <span data-ttu-id="4c5c7-114">您可以設定新的按鍵或按鍵組合，方法是指定 keycode 或 keycode 組合 (如 CTRL 或 SHIFT 鍵組合) 為 **vKeyAbort** 的值，或是藉由指定 **fAbortLeftMouse** 或 **fAbortRightMouse** 成員，將滑鼠左鍵或右鍵設定為中止索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4c5c7-114">You can set a new key or keystroke combination by specifying the keycode or keycode combination (as in a CTRL or SHIFT key combination) as the value of **vKeyAbort**, or set the left or right mouse button as the abort key by specifying the **fAbortLeftMouse** or **fAbortRightMouse** member.</span></span> <span data-ttu-id="4c5c7-115">設定這些成員之後，請使用 [ [**WM \_ CAP \_ set \_ SEQUENCE \_ SETUP**](wm-cap-set-sequence-setup.md) message (或 [**CapCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)宏) ，將更新的 **CAPTUREPARMS** 結構傳送至 [捕獲] 視窗。</span><span class="sxs-lookup"><span data-stu-id="4c5c7-115">After you set these members, send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="4c5c7-116">**VKeyAbort** 的預設值為 VK \_ ESCAPE。</span><span class="sxs-lookup"><span data-stu-id="4c5c7-116">The default value of **vKeyAbort** is VK\_ESCAPE.</span></span> <span data-ttu-id="4c5c7-117">您必須先呼叫 [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) 函數，然後再指定可中止捕捉會話的按鍵。</span><span class="sxs-lookup"><span data-stu-id="4c5c7-117">You must call the [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) function before specifying a keystroke that can abort a capture session.</span></span> <span data-ttu-id="4c5c7-118">**FAbortLeftMouse** 和 **fAbortRightMouse** 的預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="4c5c7-118">The default values of **fAbortLeftMouse** and **fAbortRightMouse** are **TRUE**.</span></span>

 

 
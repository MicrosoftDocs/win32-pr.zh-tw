---
title: '函數 (Windows Touch 輸入) '
description: 本節包含 Windows Touch 輸入的功能。
ms.assetid: 6c64ed75-37ac-47ae-b39e-bdf10d2b5211
keywords:
- Windows Touch，函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a18ba246ab8b1d228d257d32982e9afc2c418eb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024506"
---
# <a name="functions-windows-touch-input"></a><span data-ttu-id="12802-104">函數 (Windows Touch 輸入) </span><span class="sxs-lookup"><span data-stu-id="12802-104">Functions (Windows Touch Input)</span></span>

<span data-ttu-id="12802-105">本節包含 Windows Touch 輸入的功能。</span><span class="sxs-lookup"><span data-stu-id="12802-105">This section contains functions for Windows Touch input.</span></span>

<span data-ttu-id="12802-106">下列函式用於 Windows Touch 輸入。</span><span class="sxs-lookup"><span data-stu-id="12802-106">The following functions are used for Windows Touch input.</span></span>



| <span data-ttu-id="12802-107">函式</span><span class="sxs-lookup"><span data-stu-id="12802-107">Function</span></span>                                                                                               | <span data-ttu-id="12802-108">描述</span><span class="sxs-lookup"><span data-stu-id="12802-108">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12802-109">**CloseTouchInputHandle**</span><span class="sxs-lookup"><span data-stu-id="12802-109">**CloseTouchInputHandle**</span></span>](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)                                                 | <span data-ttu-id="12802-110">關閉觸控輸入控點、釋放與其相關聯的進程記憶體，並使控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="12802-110">Closes a touch input handle, frees process memory associated with it, and invalidates the handle.</span></span>                                       |
| [<span data-ttu-id="12802-111">**GetTouchInputInfo**</span><span class="sxs-lookup"><span data-stu-id="12802-111">**GetTouchInputInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)                                                         | <span data-ttu-id="12802-112">抓取與特定觸控輸入控點相關聯之觸控輸入的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="12802-112">Retrieves detailed information about touch inputs associated with a specific touch input handle.</span></span>                                        |
| [<span data-ttu-id="12802-113">**IsTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="12802-113">**IsTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-istouchwindow)                                                                 | <span data-ttu-id="12802-114">檢查指定的視窗是否具備觸控功能，並選擇性地抓取為視窗觸控功能設定的修飾詞旗標。</span><span class="sxs-lookup"><span data-stu-id="12802-114">Checks whether a specified window is touch-capable and, optionally, retrieves the modifier flags set for the window's touch capability.</span></span> |
| [<span data-ttu-id="12802-115">**RegisterTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="12802-115">**RegisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)                                                     | <span data-ttu-id="12802-116">將視窗註冊為具備觸控功能。</span><span class="sxs-lookup"><span data-stu-id="12802-116">Registers a window as being touch-capable.</span></span>                                                                                              |
| [<span data-ttu-id="12802-117">**UnregisterTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="12802-117">**UnregisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-unregistertouchwindow)                                                 | <span data-ttu-id="12802-118">註冊不再具備觸控功能的視窗。</span><span class="sxs-lookup"><span data-stu-id="12802-118">Registers a window as no longer being touch-capable.</span></span>                                                                                    |
| [<span data-ttu-id="12802-119">SendMessage、PostMessage 和相關函數</span><span class="sxs-lookup"><span data-stu-id="12802-119">SendMessage, PostMessage, and Related Functions</span></span>](sendmessage--postmessage--and-related-functions.md) | <span data-ttu-id="12802-120">包含轉送訊息的考慮。</span><span class="sxs-lookup"><span data-stu-id="12802-120">Contains considerations about forwarding messages.</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="12802-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="12802-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12802-122">Windows Touch 輸入</span><span class="sxs-lookup"><span data-stu-id="12802-122">Windows Touch Input</span></span>](multi-touch-input.md)
</dt> <dt>

[<span data-ttu-id="12802-123">Windows Touch 輸入程式設計指南</span><span class="sxs-lookup"><span data-stu-id="12802-123">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 





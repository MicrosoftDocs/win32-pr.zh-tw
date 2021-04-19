---
description: 當文字輸入面板開啟時通知視窗。
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: 'MICROSOFT_TIP_OPENING_MSG 訊息 (Peninputpanel .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987846"
---
# <a name="microsoft_tip_opening_msg-message"></a><span data-ttu-id="cefa1-103">MICROSOFT \_ 秘訣 \_ 開啟 \_ 訊息訊息</span><span class="sxs-lookup"><span data-stu-id="cefa1-103">MICROSOFT\_TIP\_OPENING\_MSG message</span></span>

<span data-ttu-id="cefa1-104">當文字輸入面板開啟時通知視窗。</span><span class="sxs-lookup"><span data-stu-id="cefa1-104">Notifies the window when the Text Input Panel is opening.</span></span>

## <a name="parameters"></a><span data-ttu-id="cefa1-105">參數</span><span class="sxs-lookup"><span data-stu-id="cefa1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cefa1-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cefa1-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cefa1-107">目前未使用，應該是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cefa1-107">Currently not used, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cefa1-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cefa1-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cefa1-109">目前未使用，應該是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cefa1-109">Currently not used, should be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cefa1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="cefa1-110">Return value</span></span>

<span data-ttu-id="cefa1-111">處理此訊息之後，應用程式應該呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 。</span><span class="sxs-lookup"><span data-stu-id="cefa1-111">Applications should call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) after handling this message.</span></span> <span data-ttu-id="cefa1-112">如需其傳回值的詳細資訊，請參閱 **DefWindowProc** 。</span><span class="sxs-lookup"><span data-stu-id="cefa1-112">See **DefWindowProc** for information about its return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="cefa1-113">備註</span><span class="sxs-lookup"><span data-stu-id="cefa1-113">Remarks</span></span>

<span data-ttu-id="cefa1-114">此通知可讓您知道何時會開啟輸入面板。</span><span class="sxs-lookup"><span data-stu-id="cefa1-114">This notification lets you know when the input panel is opening.</span></span> <span data-ttu-id="cefa1-115">如果您想要在發生這種情況時執行動作，請處理訊息、在處理常式中執行作業，然後將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="cefa1-115">If you want to perform an action when this happens, handle the message, perform your operation in the handler, and then pass on the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

> [!Note]  
> <span data-ttu-id="cefa1-116">此訊息也會在文字輸入面板已顯示，且使用者從鍵盤切換至手寫外觀時傳送。</span><span class="sxs-lookup"><span data-stu-id="cefa1-116">This message is also sent when the Text Input Panel is already visible and the user switches from the keyboard to the handwriting skin.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cefa1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cefa1-117">Requirements</span></span>



| <span data-ttu-id="cefa1-118">需求</span><span class="sxs-lookup"><span data-stu-id="cefa1-118">Requirement</span></span> | <span data-ttu-id="cefa1-119">值</span><span class="sxs-lookup"><span data-stu-id="cefa1-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cefa1-120">用戶端</span><span class="sxs-lookup"><span data-stu-id="cefa1-120">Client</span></span><br/> | <span data-ttu-id="cefa1-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cefa1-121">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="cefa1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="cefa1-122">Header</span></span><br/> | <dl> <span data-ttu-id="cefa1-123"><dt>Peninputpanel。h</dt></span><span class="sxs-lookup"><span data-stu-id="cefa1-123"><dt>Peninputpanel.h</dt></span></span> </dl> |



 


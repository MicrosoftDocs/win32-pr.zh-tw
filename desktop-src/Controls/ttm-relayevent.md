---
title: 'TTM_RELAYEVENT 訊息 (Commctrl .h) '
description: 將滑鼠訊息傳遞至工具提示控制項以進行處理。
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- TTM_RELAYEVENT message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322276"
---
# <a name="ttm_relayevent-message"></a><span data-ttu-id="54aad-104">TTM \_ RELAYEVENT 訊息</span><span class="sxs-lookup"><span data-stu-id="54aad-104">TTM\_RELAYEVENT message</span></span>

<span data-ttu-id="54aad-105">將滑鼠訊息傳遞至工具提示控制項以進行處理。</span><span class="sxs-lookup"><span data-stu-id="54aad-105">Passes a mouse message to a tooltip control for processing.</span></span>

## <a name="parameters"></a><span data-ttu-id="54aad-106">參數</span><span class="sxs-lookup"><span data-stu-id="54aad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54aad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54aad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54aad-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="54aad-108">Must be zero.</span></span> <span data-ttu-id="54aad-109">**Windows 7 和更新版本：** 如果工具提示的位置是從游標位置位移 (的順序不會被手指或指向裝置) 的阻礙，此參數可能會包含從 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息取得的額外資訊。</span><span class="sxs-lookup"><span data-stu-id="54aad-109">**Windows 7 and later:** If the position of the tooltip is offset from the cursor position (in order not be obstructed by a finger or pointing device), this parameter can contain extra information taken from the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="54aad-110">使用 [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo)取出此額外資訊。</span><span class="sxs-lookup"><span data-stu-id="54aad-110">Retrieve this extra information with [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span></span>

</dd> <dt>

<span data-ttu-id="54aad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54aad-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54aad-112">訊息 [**結構的**](/windows/win32/api/winuser/ns-winuser-msg) 指標，其中包含要轉送的訊息。</span><span class="sxs-lookup"><span data-stu-id="54aad-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to relay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54aad-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="54aad-113">Return value</span></span>

<span data-ttu-id="54aad-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="54aad-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54aad-115">備註</span><span class="sxs-lookup"><span data-stu-id="54aad-115">Remarks</span></span>

<span data-ttu-id="54aad-116">工具提示控制項只會處理 **TTM \_ RELAYEVENT** 訊息傳遞給它的下列訊息：</span><span class="sxs-lookup"><span data-stu-id="54aad-116">A tooltip control processes only the following messages passed to it by the **TTM\_RELAYEVENT** message:</span></span>

-   <span data-ttu-id="54aad-117">WM \_ LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="54aad-117">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="54aad-118">WM \_ LBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="54aad-118">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="54aad-119">WM \_ MBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="54aad-119">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="54aad-120">WM \_ MBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="54aad-120">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="54aad-121">WM \_ MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="54aad-121">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="54aad-122">WM \_ NCMOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="54aad-122">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="54aad-123">WM \_ RBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="54aad-123">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="54aad-124">WM \_ RBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="54aad-124">WM\_RBUTTONUP</span></span>

<span data-ttu-id="54aad-125">所有其他訊息都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="54aad-125">All other messages are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="54aad-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="54aad-126">Requirements</span></span>



| <span data-ttu-id="54aad-127">需求</span><span class="sxs-lookup"><span data-stu-id="54aad-127">Requirement</span></span> | <span data-ttu-id="54aad-128">值</span><span class="sxs-lookup"><span data-stu-id="54aad-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54aad-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54aad-129">Minimum supported client</span></span><br/> | <span data-ttu-id="54aad-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54aad-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54aad-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54aad-131">Minimum supported server</span></span><br/> | <span data-ttu-id="54aad-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54aad-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54aad-133">標頭</span><span class="sxs-lookup"><span data-stu-id="54aad-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="54aad-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="54aad-134"><dt>Commctrl.h</dt></span></span> </dl> |



 


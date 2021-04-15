---
title: 'WM_GETTITLEBARINFOEX 訊息 (Winuser .h) '
description: 傳送至要求延伸的標題列資訊。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384138"
---
# <a name="wm_gettitlebarinfoex-message"></a><span data-ttu-id="aa189-105">WM \_ GETTITLEBARINFOEX 訊息</span><span class="sxs-lookup"><span data-stu-id="aa189-105">WM\_GETTITLEBARINFOEX message</span></span>

<span data-ttu-id="aa189-106">傳送至要求延伸的標題列資訊。</span><span class="sxs-lookup"><span data-stu-id="aa189-106">Sent to request extended title bar information.</span></span> <span data-ttu-id="aa189-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="aa189-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a><span data-ttu-id="aa189-108">參數</span><span class="sxs-lookup"><span data-stu-id="aa189-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa189-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa189-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa189-110">未使用此參數，且必須為0。</span><span class="sxs-lookup"><span data-stu-id="aa189-110">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="aa189-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa189-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa189-112">[**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="aa189-112">A pointer to a [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) structure.</span></span> <span data-ttu-id="aa189-113">訊息寄件者負責為此結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="aa189-113">The message sender is responsible for allocating memory for this structure.</span></span> <span data-ttu-id="aa189-114">將此結構的 **cbSize** 成員設定為， `sizeof(TITLEBARINFOEX)` 然後才傳遞此結構與訊息。</span><span class="sxs-lookup"><span data-stu-id="aa189-114">Set the **cbSize** member of this structure to `sizeof(TITLEBARINFOEX)` before passing this structure with the message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa189-115">備註</span><span class="sxs-lookup"><span data-stu-id="aa189-115">Remarks</span></span>

<span data-ttu-id="aa189-116">下列範例會顯示訊息接收者如何轉換 **LPARAM** 值，以抓取 [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) 結構。</span><span class="sxs-lookup"><span data-stu-id="aa189-116">The following example shows how the message receiver casts an **LPARAM** value to retrieve the [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) structure.</span></span>

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a><span data-ttu-id="aa189-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa189-117">Requirements</span></span>



| <span data-ttu-id="aa189-118">需求</span><span class="sxs-lookup"><span data-stu-id="aa189-118">Requirement</span></span> | <span data-ttu-id="aa189-119">值</span><span class="sxs-lookup"><span data-stu-id="aa189-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa189-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa189-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa189-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa189-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aa189-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa189-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa189-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa189-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aa189-124">標頭</span><span class="sxs-lookup"><span data-stu-id="aa189-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa189-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="aa189-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa189-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa189-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa189-127">功能表總覽</span><span class="sxs-lookup"><span data-stu-id="aa189-127">Menus Overview</span></span>](menus.md)
</dt> </dl>

 


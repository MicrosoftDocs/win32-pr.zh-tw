---
title: 'EM_FMTLINES 訊息 (Winuser .h) '
description: 設定旗標，判斷多行編輯控制項是否包含軟換行字元。 軟換行是由兩個換行字元和換行字元所組成，且會插入到因為 wordwrapping 而中斷的行尾。
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- EM_FMTLINES message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c12a22ee8c30ffa74705f670a16caa3651e9b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465576"
---
# <a name="em_fmtlines-message"></a><span data-ttu-id="aa8c3-105">EM \_ FMTLINES 訊息</span><span class="sxs-lookup"><span data-stu-id="aa8c3-105">EM\_FMTLINES message</span></span>

<span data-ttu-id="aa8c3-106">設定旗標，判斷多行編輯控制項是否包含軟換行字元。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-106">Sets a flag that determines whether a multiline edit control includes soft line-break characters.</span></span> <span data-ttu-id="aa8c3-107">軟換行是由兩個換行字元和換行字元所組成，且會插入到因為 wordwrapping 而中斷的行尾。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-107">A soft line break consists of two carriage returns and a line feed and is inserted at the end of a line that is broken because of wordwrapping.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa8c3-108">參數</span><span class="sxs-lookup"><span data-stu-id="aa8c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa8c3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa8c3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa8c3-110">指定是否要插入軟換行字元。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-110">Specifies whether soft line-break characters are to be inserted.</span></span> <span data-ttu-id="aa8c3-111">**TRUE** 值會插入字元;**FALSE** 值會移除它們。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-111">A value of **TRUE** inserts the characters; a value of **FALSE** removes them.</span></span>

</dd> <dt>

<span data-ttu-id="aa8c3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa8c3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa8c3-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa8c3-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa8c3-114">Return value</span></span>

<span data-ttu-id="aa8c3-115">傳回值與 *wParam* 參數相同。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-115">The return value is identical to the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa8c3-116">備註</span><span class="sxs-lookup"><span data-stu-id="aa8c3-116">Remarks</span></span>

<span data-ttu-id="aa8c3-117">此訊息只會影響 [**EM \_ GETHANDLE**](em-gethandle.md) 訊息所傳回的緩衝區，以及由 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) 訊息傳回的文字。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-117">This message affects only the buffer returned by the [**EM\_GETHANDLE**](em-gethandle.md) message and the text returned by the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext) message.</span></span> <span data-ttu-id="aa8c3-118">它不會影響編輯控制項內的文字顯示方式。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-118">It has no effect on the display of the text within the edit control.</span></span>

<span data-ttu-id="aa8c3-119">**EM \_ FMTLINES** 訊息不會影響以硬換行結尾的行。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-119">The **EM\_FMTLINES** message does not affect a line that ends with a hard line break.</span></span> <span data-ttu-id="aa8c3-120">硬換行是由一個換行字元和一個換行字元所組成。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-120">A hard line break consists of one carriage return and a line feed.</span></span>

> [!Note]  
> <span data-ttu-id="aa8c3-121">處理此訊息時，文字會變更的大小。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-121">The size of the text changes when this message is processed.</span></span>

 

<span data-ttu-id="aa8c3-122">**Rich Edit：** 不支援 **EM \_ FMTLINES** 訊息。</span><span class="sxs-lookup"><span data-stu-id="aa8c3-122">**Rich Edit:** The **EM\_FMTLINES** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa8c3-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa8c3-123">Requirements</span></span>



| <span data-ttu-id="aa8c3-124">需求</span><span class="sxs-lookup"><span data-stu-id="aa8c3-124">Requirement</span></span> | <span data-ttu-id="aa8c3-125">值</span><span class="sxs-lookup"><span data-stu-id="aa8c3-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa8c3-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa8c3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aa8c3-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa8c3-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aa8c3-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa8c3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aa8c3-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa8c3-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aa8c3-130">標頭</span><span class="sxs-lookup"><span data-stu-id="aa8c3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa8c3-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="aa8c3-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa8c3-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa8c3-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa8c3-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="aa8c3-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aa8c3-134">**EM \_ GETHANDLE**</span><span class="sxs-lookup"><span data-stu-id="aa8c3-134">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

<span data-ttu-id="aa8c3-135">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="aa8c3-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="aa8c3-136">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="aa8c3-136">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 


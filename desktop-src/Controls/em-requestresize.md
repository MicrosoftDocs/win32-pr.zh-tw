---
title: 'EM_REQUESTRESIZE 訊息 (Richedit .h) '
description: 強制 rich edit 控制項將 EN \_ REQUESTRESIZE 通知程式碼傳送至其父視窗。
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- EM_REQUESTRESIZE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187312"
---
# <a name="em_requestresize-message"></a><span data-ttu-id="a32f4-104">EM \_ REQUESTRESIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="a32f4-104">EM\_REQUESTRESIZE message</span></span>

<span data-ttu-id="a32f4-105">強制 rich edit 控制項將 [**EN \_ REQUESTRESIZE**](en-requestresize.md) 通知程式碼傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="a32f4-105">Forces a rich edit control to send an [**EN\_REQUESTRESIZE**](en-requestresize.md) notification code to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="a32f4-106">參數</span><span class="sxs-lookup"><span data-stu-id="a32f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a32f4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a32f4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a32f4-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="a32f4-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a32f4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a32f4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a32f4-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="a32f4-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a32f4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a32f4-111">Return value</span></span>

<span data-ttu-id="a32f4-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a32f4-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a32f4-113">備註</span><span class="sxs-lookup"><span data-stu-id="a32f4-113">Remarks</span></span>

<span data-ttu-id="a32f4-114">此訊息在無底邊 rich edit 控制項父系的 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 處理期間很有用。</span><span class="sxs-lookup"><span data-stu-id="a32f4-114">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a32f4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a32f4-115">Requirements</span></span>



| <span data-ttu-id="a32f4-116">需求</span><span class="sxs-lookup"><span data-stu-id="a32f4-116">Requirement</span></span> | <span data-ttu-id="a32f4-117">值</span><span class="sxs-lookup"><span data-stu-id="a32f4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a32f4-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a32f4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a32f4-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a32f4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a32f4-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a32f4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a32f4-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a32f4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a32f4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a32f4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a32f4-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="a32f4-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a32f4-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a32f4-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="a32f4-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="a32f4-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a32f4-126">**EN \_ REQUESTRESIZE**</span><span class="sxs-lookup"><span data-stu-id="a32f4-126">**EN\_REQUESTRESIZE**</span></span>](en-requestresize.md)
</dt> <dt>

<span data-ttu-id="a32f4-127">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="a32f4-127">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a32f4-128">**WM \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="a32f4-128">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 


---
title: 'DM_REPOSITION 訊息 (Winuser .h) '
description: 重新置放最上層對話方塊，使其符合桌面上的範圍。 應用程式可以在調整大小後將此訊息傳送至對話方塊，以確保整個對話方塊保持可見。
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- DM_REPOSITION 訊息對話方塊
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025451"
---
# <a name="dm_reposition-message"></a><span data-ttu-id="41334-105">DM 重新 \_ 調整訊息</span><span class="sxs-lookup"><span data-stu-id="41334-105">DM\_REPOSITION message</span></span>

<span data-ttu-id="41334-106">重新置放最上層對話方塊，使其符合桌面上的範圍。</span><span class="sxs-lookup"><span data-stu-id="41334-106">Repositions a top-level dialog box so that it fits within the desktop area.</span></span> <span data-ttu-id="41334-107">應用程式可以在調整大小後將此訊息傳送至對話方塊，以確保整個對話方塊保持可見。</span><span class="sxs-lookup"><span data-stu-id="41334-107">An application can send this message to a dialog box after resizing it to ensure that the entire dialog box remains visible.</span></span>


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a><span data-ttu-id="41334-108">參數</span><span class="sxs-lookup"><span data-stu-id="41334-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41334-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41334-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41334-110">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="41334-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="41334-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41334-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41334-112">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="41334-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41334-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="41334-113">Return value</span></span>

<span data-ttu-id="41334-114">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="41334-114">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41334-115">備註</span><span class="sxs-lookup"><span data-stu-id="41334-115">Remarks</span></span>

<span data-ttu-id="41334-116">如果對話方塊是子視窗，則此訊息不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="41334-116">This message has no effect if the dialog box is a child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="41334-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="41334-117">Requirements</span></span>



| <span data-ttu-id="41334-118">需求</span><span class="sxs-lookup"><span data-stu-id="41334-118">Requirement</span></span> | <span data-ttu-id="41334-119">值</span><span class="sxs-lookup"><span data-stu-id="41334-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41334-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41334-120">Minimum supported client</span></span><br/> | <span data-ttu-id="41334-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41334-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="41334-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41334-122">Minimum supported server</span></span><br/> | <span data-ttu-id="41334-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41334-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41334-124">標頭</span><span class="sxs-lookup"><span data-stu-id="41334-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="41334-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="41334-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41334-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41334-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41334-127">對話方塊概觀</span><span class="sxs-lookup"><span data-stu-id="41334-127">Dialog Boxes Overview</span></span>](dialog-boxes.md)
</dt> </dl>

 

 






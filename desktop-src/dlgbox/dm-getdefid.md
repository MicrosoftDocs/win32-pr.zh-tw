---
title: 'DM_GETDEFID 訊息 (Winuser .h) '
description: 抓取對話方塊的預設按鈕控制項識別碼。
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- DM_GETDEFID 訊息對話方塊
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fdcdfc2cd278ab452d48ecb1c254bdb00ffbb7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509311"
---
# <a name="dm_getdefid-message"></a><span data-ttu-id="247c1-104">DM \_ GETDEFID 訊息</span><span class="sxs-lookup"><span data-stu-id="247c1-104">DM\_GETDEFID message</span></span>

<span data-ttu-id="247c1-105">抓取對話方塊的預設按鈕控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="247c1-105">Retrieves the identifier of the default push button control for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
```



## <a name="parameters"></a><span data-ttu-id="247c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="247c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="247c1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="247c1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="247c1-108">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="247c1-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="247c1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="247c1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="247c1-110">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="247c1-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="247c1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="247c1-111">Return value</span></span>

<span data-ttu-id="247c1-112">如果預設的 [推送] 按鈕存在，則傳回值的高序位文字會包含值 **DC \_ HASDEFID** ，而低序位單字則包含控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="247c1-112">If a default push button exists, the high-order word of the return value contains the value **DC\_HASDEFID** and the low-order word contains the control identifier.</span></span> <span data-ttu-id="247c1-113">否則，傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="247c1-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="247c1-114">備註</span><span class="sxs-lookup"><span data-stu-id="247c1-114">Remarks</span></span>

<span data-ttu-id="247c1-115">[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)函式會處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="247c1-115">The [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="247c1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="247c1-116">Requirements</span></span>



| <span data-ttu-id="247c1-117">需求</span><span class="sxs-lookup"><span data-stu-id="247c1-117">Requirement</span></span> | <span data-ttu-id="247c1-118">值</span><span class="sxs-lookup"><span data-stu-id="247c1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="247c1-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="247c1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="247c1-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="247c1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="247c1-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="247c1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="247c1-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="247c1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="247c1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="247c1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="247c1-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="247c1-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="247c1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="247c1-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="247c1-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="247c1-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="247c1-127">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="247c1-127">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="247c1-128">**DM \_ SETDEFID**</span><span class="sxs-lookup"><span data-stu-id="247c1-128">**DM\_SETDEFID**</span></span>](dm-setdefid.md)
</dt> <dt>

<span data-ttu-id="247c1-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="247c1-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="247c1-130">對話方塊</span><span class="sxs-lookup"><span data-stu-id="247c1-130">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

 






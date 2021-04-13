---
title: 'EM_INSERTIMAGE 訊息 (Richedit .h) '
description: 以顯示影像的 blob 取代選取範圍。
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- EM_INSERTIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464536"
---
# <a name="em_insertimage-message"></a><span data-ttu-id="6640c-104">EM \_ INSERTIMAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="6640c-104">EM\_INSERTIMAGE message</span></span>

<span data-ttu-id="6640c-105">以顯示影像的 blob 取代選取範圍。</span><span class="sxs-lookup"><span data-stu-id="6640c-105">Replaces the selection with a blob that displays an image.</span></span>


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a><span data-ttu-id="6640c-106">參數</span><span class="sxs-lookup"><span data-stu-id="6640c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6640c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6640c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6640c-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="6640c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6640c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6640c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6640c-110">包含映射 blob 的 [**RICHEDIT \_ 影像 \_ 參數**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="6640c-110">A pointer to a [**RICHEDIT\_IMAGE\_PARAMETERS**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) structure that contains the image blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6640c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6640c-111">Return value</span></span>

<span data-ttu-id="6640c-112">\_如果成功，則傳回 S OK，或下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6640c-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="6640c-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6640c-113">Return code</span></span>                                                                                    | <span data-ttu-id="6640c-114">Description</span><span class="sxs-lookup"><span data-stu-id="6640c-114">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="6640c-115"><dt>**E \_失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="6640c-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="6640c-116">無法插入影像。</span><span class="sxs-lookup"><span data-stu-id="6640c-116">Cannot insert the image.</span></span> <br/>                          |
| <dl> <span data-ttu-id="6640c-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6640c-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="6640c-118">*LParam* 參數為 Null 或指向不正確影像。</span><span class="sxs-lookup"><span data-stu-id="6640c-118">The *lParam* parameter is NULL or points to an invalid image.</span></span> |
| <dl> <span data-ttu-id="6640c-119"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6640c-119"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="6640c-120">可用的記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="6640c-120">Insufficient memory is available.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="6640c-121">備註</span><span class="sxs-lookup"><span data-stu-id="6640c-121">Remarks</span></span>

<span data-ttu-id="6640c-122">如果選取範圍是插入點，則會在插入點插入映射 blob。</span><span class="sxs-lookup"><span data-stu-id="6640c-122">If the selection is an insertion point, the image blob is inserted at the insertion point.</span></span>

## <a name="requirements"></a><span data-ttu-id="6640c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6640c-123">Requirements</span></span>



| <span data-ttu-id="6640c-124">需求</span><span class="sxs-lookup"><span data-stu-id="6640c-124">Requirement</span></span> | <span data-ttu-id="6640c-125">值</span><span class="sxs-lookup"><span data-stu-id="6640c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6640c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6640c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6640c-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6640c-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6640c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6640c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6640c-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6640c-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6640c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="6640c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6640c-131"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6640c-131"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6640c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6640c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6640c-133">**EM \_ INSERTTABLE**</span><span class="sxs-lookup"><span data-stu-id="6640c-133">**EM\_INSERTTABLE**</span></span>](em-inserttable.md)
</dt> </dl>

 

 






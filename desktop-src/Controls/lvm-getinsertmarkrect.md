---
title: 'LVM_GETINSERTMARKRECT 訊息 (Commctrl .h) '
description: 抓取插入點界限的矩形。
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- LVM_GETINSERTMARKRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd85bfb94f6425d2666372fd141b531fcb238643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934901"
---
# <a name="lvm_getinsertmarkrect-message"></a><span data-ttu-id="82f5a-104">LVM \_ GETINSERTMARKRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="82f5a-104">LVM\_GETINSERTMARKRECT message</span></span>

<span data-ttu-id="82f5a-105">抓取插入點界限的矩形。</span><span class="sxs-lookup"><span data-stu-id="82f5a-105">Retrieves the rectangle that bounds the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="82f5a-106">參數</span><span class="sxs-lookup"><span data-stu-id="82f5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82f5a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82f5a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="82f5a-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="82f5a-108">Not used; must be zero.</span></span></dd> <dt>

<span data-ttu-id="82f5a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82f5a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="82f5a-110"><a href="/previous-versions//dd162897(v=vs.85)">**矩形結構的**</a>指標，其中包含包圍插入點之矩形的座標。</span><span class="sxs-lookup"><span data-stu-id="82f5a-110">Pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure that contains the coordinates of a rectangle that bounds the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82f5a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="82f5a-111">Return value</span></span>

<span data-ttu-id="82f5a-112">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="82f5a-112">Returns one of the following values.</span></span>



| <span data-ttu-id="82f5a-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="82f5a-113">Return code</span></span>                                                                      | <span data-ttu-id="82f5a-114">Description</span><span class="sxs-lookup"><span data-stu-id="82f5a-114">Description</span></span>                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="82f5a-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="82f5a-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="82f5a-116">找不到插入點。</span><span class="sxs-lookup"><span data-stu-id="82f5a-116">No insertion point found.</span></span><br/> |
| <dl> <span data-ttu-id="82f5a-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="82f5a-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="82f5a-118">找到插入點。</span><span class="sxs-lookup"><span data-stu-id="82f5a-118">Insertion point found.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="82f5a-119">備註</span><span class="sxs-lookup"><span data-stu-id="82f5a-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="82f5a-120">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="82f5a-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="82f5a-121">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="82f5a-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="82f5a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="82f5a-122">Requirements</span></span>



| <span data-ttu-id="82f5a-123">需求</span><span class="sxs-lookup"><span data-stu-id="82f5a-123">Requirement</span></span> | <span data-ttu-id="82f5a-124">值</span><span class="sxs-lookup"><span data-stu-id="82f5a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82f5a-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82f5a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="82f5a-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82f5a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82f5a-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82f5a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="82f5a-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82f5a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82f5a-129">標頭</span><span class="sxs-lookup"><span data-stu-id="82f5a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="82f5a-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="82f5a-130"><dt>Commctrl.h</dt></span></span> </dl> |



 


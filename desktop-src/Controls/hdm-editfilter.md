---
title: 'HDM_EDITFILTER 訊息 (Commctrl .h) '
description: 當篩選按鈕具有焦點時，將輸入焦點移至編輯方塊。
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- HDM_EDITFILTER message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733c79bf747d3b55aa8dd38eb8fad8fdc83601e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686103"
---
# <a name="hdm_editfilter-message"></a><span data-ttu-id="a8bb4-104">HDM \_ EDITFILTER 訊息</span><span class="sxs-lookup"><span data-stu-id="a8bb4-104">HDM\_EDITFILTER message</span></span>

<span data-ttu-id="a8bb4-105">當篩選按鈕具有焦點時，將輸入焦點移至編輯方塊。</span><span class="sxs-lookup"><span data-stu-id="a8bb4-105">Moves the input focus to the edit box when a filter button has the focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8bb4-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8bb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8bb4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8bb4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8bb4-108">值，指定要編輯的資料行。</span><span class="sxs-lookup"><span data-stu-id="a8bb4-108">A value specifying the column to edit.</span></span>

</dd> <dt>

<span data-ttu-id="a8bb4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8bb4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8bb4-110">指定如何處理使用者編輯變更的旗標。</span><span class="sxs-lookup"><span data-stu-id="a8bb4-110">A flag that specifies how to handle the user's editing changes.</span></span> <span data-ttu-id="a8bb4-111">使用此旗標來指定當使用者在傳送訊息時編輯篩選器的過程中，該怎麼辦。</span><span class="sxs-lookup"><span data-stu-id="a8bb4-111">Use this flag to specify what to do if the user is in the process of editing the filter when the message is sent.</span></span>



| <span data-ttu-id="a8bb4-112">值</span><span class="sxs-lookup"><span data-stu-id="a8bb4-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="a8bb4-113">意義</span><span class="sxs-lookup"><span data-stu-id="a8bb4-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="a8bb4-114"><dt></dt><dt> **TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="a8bb4-114"><dt></dt> <dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="a8bb4-115">捨棄使用者所做的變更。</span><span class="sxs-lookup"><span data-stu-id="a8bb4-115">Discard the changes made by the user.</span></span> <br/> |
| <dl> <span data-ttu-id="a8bb4-116"><dt></dt><dt> **FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="a8bb4-116"><dt></dt> <dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="a8bb4-117">接受使用者所做的變更。</span><span class="sxs-lookup"><span data-stu-id="a8bb4-117">Accept the changes made by the user.</span></span> <br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8bb4-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8bb4-118">Return value</span></span>

<span data-ttu-id="a8bb4-119">傳回整數。</span><span class="sxs-lookup"><span data-stu-id="a8bb4-119">Returns an integer.</span></span> <span data-ttu-id="a8bb4-120">**LRESULT** 會轉換為整數，表示 **TRUE** (1) 或 **FALSE** (0) 。</span><span class="sxs-lookup"><span data-stu-id="a8bb4-120">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8bb4-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8bb4-121">Requirements</span></span>



| <span data-ttu-id="a8bb4-122">需求</span><span class="sxs-lookup"><span data-stu-id="a8bb4-122">Requirement</span></span> | <span data-ttu-id="a8bb4-123">值</span><span class="sxs-lookup"><span data-stu-id="a8bb4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bb4-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8bb4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a8bb4-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8bb4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8bb4-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8bb4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a8bb4-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8bb4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8bb4-128">標頭</span><span class="sxs-lookup"><span data-stu-id="a8bb4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8bb4-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8bb4-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8bb4-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8bb4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bb4-131">**HDM \_ CLEARFILTER**</span><span class="sxs-lookup"><span data-stu-id="a8bb4-131">**HDM\_CLEARFILTER**</span></span>](hdm-clearfilter.md)
</dt> </dl>

 

 






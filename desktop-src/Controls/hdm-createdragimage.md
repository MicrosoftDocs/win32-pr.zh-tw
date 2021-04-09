---
title: 'HDM_CREATEDRAGIMAGE 訊息 (Commctrl .h) '
description: 建立專案影像的半透明版本，作為拖曳影像使用。 您可以明確地傳送此訊息，或使用標頭 \_ CreateDragImage 宏。
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- HDM_CREATEDRAGIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025254"
---
# <a name="hdm_createdragimage-message"></a><span data-ttu-id="6137f-105">HDM \_ CREATEDRAGIMAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="6137f-105">HDM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="6137f-106">建立專案影像的半透明版本，作為拖曳影像使用。</span><span class="sxs-lookup"><span data-stu-id="6137f-106">Creates a semi-transparent version of an item's image for use as a dragging image.</span></span> <span data-ttu-id="6137f-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) 宏。</span><span class="sxs-lookup"><span data-stu-id="6137f-107">You can send this message explicitly or use the [**Header\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6137f-108">參數</span><span class="sxs-lookup"><span data-stu-id="6137f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6137f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6137f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6137f-110">標題控制項中專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="6137f-110">The zero-based index of the item within the header control.</span></span> <span data-ttu-id="6137f-111">指派給此專案的影像是透明影像的基礎。</span><span class="sxs-lookup"><span data-stu-id="6137f-111">The image assigned to this item is the basis for the transparent image.</span></span>

</dd> <dt>

<span data-ttu-id="6137f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6137f-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6137f-113">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6137f-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6137f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6137f-114">Return value</span></span>

<span data-ttu-id="6137f-115">傳回影像清單的控制碼，其中包含新的影像做為其唯一的元素。</span><span class="sxs-lookup"><span data-stu-id="6137f-115">Returns a handle to an image list that contains the new image as its only element.</span></span>

## <a name="requirements"></a><span data-ttu-id="6137f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6137f-116">Requirements</span></span>



| <span data-ttu-id="6137f-117">需求</span><span class="sxs-lookup"><span data-stu-id="6137f-117">Requirement</span></span> | <span data-ttu-id="6137f-118">值</span><span class="sxs-lookup"><span data-stu-id="6137f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6137f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6137f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6137f-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6137f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6137f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6137f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6137f-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6137f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6137f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6137f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6137f-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6137f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






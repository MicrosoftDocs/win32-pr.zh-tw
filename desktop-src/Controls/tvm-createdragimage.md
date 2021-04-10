---
title: 'TVM_CREATEDRAGIMAGE 訊息 (Commctrl .h) '
description: 在樹狀檢視控制項中，為指定的專案建立拖曳點陣圖。
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- TVM_CREATEDRAGIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103902"
---
# <a name="tvm_createdragimage-message"></a><span data-ttu-id="d56a9-104">TVM \_ CREATEDRAGIMAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="d56a9-104">TVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="d56a9-105">在樹狀檢視控制項中，為指定的專案建立拖曳點陣圖。</span><span class="sxs-lookup"><span data-stu-id="d56a9-105">Creates a dragging bitmap for the specified item in a tree-view control.</span></span> <span data-ttu-id="d56a9-106">此訊息也會建立點陣圖的影像清單，並將點陣圖加入影像清單中。</span><span class="sxs-lookup"><span data-stu-id="d56a9-106">The message also creates an image list for the bitmap and adds the bitmap to the image list.</span></span> <span data-ttu-id="d56a9-107">應用程式可以在使用影像清單函式拖曳專案時顯示影像。</span><span class="sxs-lookup"><span data-stu-id="d56a9-107">An application can display the image when dragging the item by using the image list functions.</span></span> <span data-ttu-id="d56a9-108">您可以使用 [**TreeView \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d56a9-108">You can send this message explicitly or by using the [**TreeView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d56a9-109">參數</span><span class="sxs-lookup"><span data-stu-id="d56a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d56a9-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d56a9-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d56a9-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d56a9-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d56a9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d56a9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d56a9-113">接收新拖曳點陣圖之專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d56a9-113">Handle to the item that receives the new dragging bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d56a9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d56a9-114">Return value</span></span>

<span data-ttu-id="d56a9-115">如果成功，則傳回已加入拖曳點陣圖之影像清單的控制碼，否則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d56a9-115">Returns the handle to the image list to which the dragging bitmap was added if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d56a9-116">備註</span><span class="sxs-lookup"><span data-stu-id="d56a9-116">Remarks</span></span>

<span data-ttu-id="d56a9-117">如果您在沒有相關聯影像清單的情況下建立樹狀檢視控制項，則無法使用 **TVM \_ CREATEDRAGIMAGE** 訊息來建立要在拖曳作業期間顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="d56a9-117">If you create a tree-view control without an associated image list, you cannot use the **TVM\_CREATEDRAGIMAGE** message to create the image to display during a drag operation.</span></span> <span data-ttu-id="d56a9-118">您必須執行您自己的方法來建立拖曳游標。</span><span class="sxs-lookup"><span data-stu-id="d56a9-118">You must implement your own method of creating a drag cursor.</span></span>

<span data-ttu-id="d56a9-119">當不再需要時，您的應用程式會負責終結影像清單。</span><span class="sxs-lookup"><span data-stu-id="d56a9-119">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d56a9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d56a9-120">Requirements</span></span>



| <span data-ttu-id="d56a9-121">需求</span><span class="sxs-lookup"><span data-stu-id="d56a9-121">Requirement</span></span> | <span data-ttu-id="d56a9-122">值</span><span class="sxs-lookup"><span data-stu-id="d56a9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d56a9-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d56a9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d56a9-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d56a9-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d56a9-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d56a9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d56a9-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d56a9-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d56a9-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d56a9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d56a9-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d56a9-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






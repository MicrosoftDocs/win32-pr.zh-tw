---
title: 'LVM_SETITEMPOSITION32 訊息 (Commctrl .h) '
description: 將專案移至清單視圖控制項中的指定位置 (必須是圖示或小圖示視圖) 。
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- LVM_SETITEMPOSITION32 message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025154"
---
# <a name="lvm_setitemposition32-message"></a><span data-ttu-id="f6d0e-104">LVM \_ SETITEMPOSITION32 訊息</span><span class="sxs-lookup"><span data-stu-id="f6d0e-104">LVM\_SETITEMPOSITION32 message</span></span>

<span data-ttu-id="f6d0e-105">將專案移至清單視圖控制項中的指定位置 (必須是圖示或小圖示視圖) 。</span><span class="sxs-lookup"><span data-stu-id="f6d0e-105">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="f6d0e-106">這則訊息與 [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) 訊息不同，因為它使用32位的座標。</span><span class="sxs-lookup"><span data-stu-id="f6d0e-106">This message differs from the [**LVM\_SETITEMPOSITION**](lvm-setitemposition.md) message in that it uses 32-bit coordinates.</span></span> <span data-ttu-id="f6d0e-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="f6d0e-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6d0e-108">參數</span><span class="sxs-lookup"><span data-stu-id="f6d0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6d0e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6d0e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6d0e-110">要設定其位置之清單視圖專案的索引。</span><span class="sxs-lookup"><span data-stu-id="f6d0e-110">Index of the list-view item for which to set the position.</span></span>

</dd> <dt>

<span data-ttu-id="f6d0e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6d0e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6d0e-112">[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，其中包含專案的新位置，以清單視圖座標為單位。</span><span class="sxs-lookup"><span data-stu-id="f6d0e-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the new position of the item, in list-view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6d0e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6d0e-113">Return value</span></span>

<span data-ttu-id="f6d0e-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="f6d0e-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6d0e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6d0e-115">Requirements</span></span>



| <span data-ttu-id="f6d0e-116">需求</span><span class="sxs-lookup"><span data-stu-id="f6d0e-116">Requirement</span></span> | <span data-ttu-id="f6d0e-117">值</span><span class="sxs-lookup"><span data-stu-id="f6d0e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d0e-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6d0e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f6d0e-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6d0e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6d0e-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6d0e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f6d0e-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6d0e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6d0e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f6d0e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6d0e-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6d0e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 


---
title: 'CBEM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 設定 ComboBoxEx 控制項的影像清單。
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935017"
---
# <a name="cbem_setimagelist-message"></a><span data-ttu-id="7ba1f-104">CBEM \_ SETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="7ba1f-104">CBEM\_SETIMAGELIST message</span></span>

<span data-ttu-id="7ba1f-105">設定 ComboBoxEx 控制項的影像清單。</span><span class="sxs-lookup"><span data-stu-id="7ba1f-105">Sets an image list for a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ba1f-106">參數</span><span class="sxs-lookup"><span data-stu-id="7ba1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ba1f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ba1f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7ba1f-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7ba1f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7ba1f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ba1f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ba1f-110">要為控制項設定之影像清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7ba1f-110">A handle to the image list to be set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ba1f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ba1f-111">Return value</span></span>

<span data-ttu-id="7ba1f-112">將控制碼傳回至先前與控制項相關聯的影像清單，如果先前未設定任何影像清單，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="7ba1f-112">Returns the handle to the image list previously associated with the control, or returns **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ba1f-113">備註</span><span class="sxs-lookup"><span data-stu-id="7ba1f-113">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7ba1f-114">影像清單中的影像高度可能會變更 ComboBoxEx 控制項的大小需求。</span><span class="sxs-lookup"><span data-stu-id="7ba1f-114">The height of images in your image list might change the size requirements of the ComboBoxEx control.</span></span> <span data-ttu-id="7ba1f-115">建議您在傳送此訊息之後調整控制項的大小，以確保顯示正確。</span><span class="sxs-lookup"><span data-stu-id="7ba1f-115">It is recommended that you resize the control after sending this message to ensure that it is displayed properly.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ba1f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ba1f-116">Requirements</span></span>



| <span data-ttu-id="7ba1f-117">需求</span><span class="sxs-lookup"><span data-stu-id="7ba1f-117">Requirement</span></span> | <span data-ttu-id="7ba1f-118">值</span><span class="sxs-lookup"><span data-stu-id="7ba1f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba1f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ba1f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba1f-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ba1f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ba1f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ba1f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba1f-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ba1f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ba1f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7ba1f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ba1f-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ba1f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






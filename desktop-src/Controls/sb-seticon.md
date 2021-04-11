---
title: 'SB_SETICON 訊息 (Commctrl .h) '
description: 設定狀態列中元件的圖示。
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- SB_SETICON message Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843996"
---
# <a name="sb_seticon-message"></a><span data-ttu-id="26aac-104">SB \_ SETICON 訊息</span><span class="sxs-lookup"><span data-stu-id="26aac-104">SB\_SETICON message</span></span>

<span data-ttu-id="26aac-105">設定狀態列中元件的圖示。</span><span class="sxs-lookup"><span data-stu-id="26aac-105">Sets the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="26aac-106">參數</span><span class="sxs-lookup"><span data-stu-id="26aac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26aac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26aac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26aac-108">將接收圖示之元件以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="26aac-108">Zero-based index of the part that will receive the icon.</span></span> <span data-ttu-id="26aac-109">如果此參數為-1，則會假設狀態列為簡單的狀態列。</span><span class="sxs-lookup"><span data-stu-id="26aac-109">If this parameter is -1, the status bar is assumed to be a simple status bar.</span></span>

</dd> <dt>

<span data-ttu-id="26aac-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26aac-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26aac-111">要設定之圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="26aac-111">Handle to the icon to be set.</span></span> <span data-ttu-id="26aac-112">如果這個值為 **Null**，則會從元件中移除圖示。</span><span class="sxs-lookup"><span data-stu-id="26aac-112">If this value is **NULL**, the icon is removed from the part.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26aac-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="26aac-113">Return value</span></span>

<span data-ttu-id="26aac-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="26aac-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="26aac-115">備註</span><span class="sxs-lookup"><span data-stu-id="26aac-115">Remarks</span></span>

<span data-ttu-id="26aac-116">狀態列不會摧毀圖示。</span><span class="sxs-lookup"><span data-stu-id="26aac-116">The status bar will not destroy the icon.</span></span> <span data-ttu-id="26aac-117">呼叫應用程式負責追蹤和終結任何圖示。</span><span class="sxs-lookup"><span data-stu-id="26aac-117">It is the calling application's responsibility to keep track of and destroy any icons.</span></span>

## <a name="requirements"></a><span data-ttu-id="26aac-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="26aac-118">Requirements</span></span>



| <span data-ttu-id="26aac-119">需求</span><span class="sxs-lookup"><span data-stu-id="26aac-119">Requirement</span></span> | <span data-ttu-id="26aac-120">值</span><span class="sxs-lookup"><span data-stu-id="26aac-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26aac-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26aac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26aac-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26aac-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26aac-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26aac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26aac-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26aac-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26aac-125">標頭</span><span class="sxs-lookup"><span data-stu-id="26aac-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="26aac-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="26aac-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






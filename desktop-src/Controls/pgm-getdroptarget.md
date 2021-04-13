---
title: 'PGM_GETDROPTARGET 訊息 (Commctrl .h) '
description: 抓取呼機控制項的 IDropTarget 介面指標。 您可以明確地傳送此訊息，或使用呼叫器 \_ GetDropTarget 宏。
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- PGM_GETDROPTARGET message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466096"
---
# <a name="pgm_getdroptarget-message"></a><span data-ttu-id="6bb7b-105">PGM \_ GETDROPTARGET 訊息</span><span class="sxs-lookup"><span data-stu-id="6bb7b-105">PGM\_GETDROPTARGET message</span></span>

<span data-ttu-id="6bb7b-106">抓取呼機控制項的 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="6bb7b-106">Retrieves a pager control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span> <span data-ttu-id="6bb7b-107">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) 宏。</span><span class="sxs-lookup"><span data-stu-id="6bb7b-107">You can send this message explicitly or use the [**Pager\_GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6bb7b-108">參數</span><span class="sxs-lookup"><span data-stu-id="6bb7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb7b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6bb7b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6bb7b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6bb7b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6bb7b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6bb7b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bb7b-112">[**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget)指標的指標，該指標會接收介面指標。</span><span class="sxs-lookup"><span data-stu-id="6bb7b-112">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="6bb7b-113">當不再需要時，呼叫端會負責呼叫這個指標的 [**發行**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="6bb7b-113">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb7b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6bb7b-114">Return value</span></span>

<span data-ttu-id="6bb7b-115">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="6bb7b-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb7b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bb7b-116">Requirements</span></span>



| <span data-ttu-id="6bb7b-117">需求</span><span class="sxs-lookup"><span data-stu-id="6bb7b-117">Requirement</span></span> | <span data-ttu-id="6bb7b-118">值</span><span class="sxs-lookup"><span data-stu-id="6bb7b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb7b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb7b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb7b-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bb7b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6bb7b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bb7b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb7b-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bb7b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6bb7b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6bb7b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bb7b-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6bb7b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 


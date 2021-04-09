---
title: 'TVM_HITTEST 訊息 (Commctrl .h) '
description: 判斷指定點相對於樹狀檢視控制項工作區的位置。 您可以使用 TreeView System.windows.media.visualtreehelper.hittest 宏明確地傳送此訊息 \_ 。
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- TVM_HITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b91a11892a2bb904d2cd7d82b5b08cea18331b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024836"
---
# <a name="tvm_hittest-message"></a><span data-ttu-id="1be7b-105">TVM \_ system.windows.media.visualtreehelper.hittest 訊息</span><span class="sxs-lookup"><span data-stu-id="1be7b-105">TVM\_HITTEST message</span></span>

<span data-ttu-id="1be7b-106">判斷指定點相對於樹狀檢視控制項工作區的位置。</span><span class="sxs-lookup"><span data-stu-id="1be7b-106">Determines the location of the specified point relative to the client area of a tree-view control.</span></span> <span data-ttu-id="1be7b-107">您可以使用 [**TreeView \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1be7b-107">You can send this message explicitly or by using the [**TreeView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1be7b-108">參數</span><span class="sxs-lookup"><span data-stu-id="1be7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1be7b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1be7b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1be7b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1be7b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1be7b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1be7b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1be7b-112">[**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1be7b-112">Pointer to a [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) structure.</span></span> <span data-ttu-id="1be7b-113">傳送訊息時， **pt** 成員會指定要測試之點的座標。</span><span class="sxs-lookup"><span data-stu-id="1be7b-113">When the message is sent, the **pt** member specifies the coordinates of the point to test.</span></span> <span data-ttu-id="1be7b-114">當訊息傳回時， **hItem** 成員是位於指定點之專案的控制碼; 如果沒有任何專案佔用點，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1be7b-114">When the message returns, the **hItem** member is the handle to the item at the specified point or **NULL** if no item occupies the point.</span></span> <span data-ttu-id="1be7b-115">此外，當訊息傳回時， **旗標** 成員是點擊測試值，指出指定點的位置。</span><span class="sxs-lookup"><span data-stu-id="1be7b-115">Also, when the message returns, the **flags** member is a hit test value that indicates the location of the specified point.</span></span> <span data-ttu-id="1be7b-116">如需點擊測試值的清單，請參閱 **TVHITTESTINFO** 結構的描述。</span><span class="sxs-lookup"><span data-stu-id="1be7b-116">For a list of hit test values, see the description of the **TVHITTESTINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1be7b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="1be7b-117">Return value</span></span>

<span data-ttu-id="1be7b-118">傳回佔據指定點之樹狀檢視專案的控制碼; 如果沒有任何專案佔用點，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1be7b-118">Returns the handle to the tree-view item that occupies the specified point, or **NULL** if no item occupies the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="1be7b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1be7b-119">Requirements</span></span>



| <span data-ttu-id="1be7b-120">需求</span><span class="sxs-lookup"><span data-stu-id="1be7b-120">Requirement</span></span> | <span data-ttu-id="1be7b-121">值</span><span class="sxs-lookup"><span data-stu-id="1be7b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1be7b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1be7b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1be7b-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1be7b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1be7b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1be7b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1be7b-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1be7b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1be7b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="1be7b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1be7b-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1be7b-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: 'TVM_GETINDENT 訊息 (Commctrl .h) '
description: 以圖元為單位，抓取子專案相對於其父代專案的縮排量（以圖元為單位）。 您可以使用 TreeView setindent 宏明確地傳送此訊息 \_ 。
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- TVM_GETINDENT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844251"
---
# <a name="tvm_getindent-message"></a><span data-ttu-id="5d872-105">TVM \_ setindent 訊息</span><span class="sxs-lookup"><span data-stu-id="5d872-105">TVM\_GETINDENT message</span></span>

<span data-ttu-id="5d872-106">以圖元為單位，抓取子專案相對於其父代專案的縮排量（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5d872-106">Retrieves the amount, in pixels, that child items are indented relative to their parent items.</span></span> <span data-ttu-id="5d872-107">您可以使用 [**TreeView \_ setindent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="5d872-107">You can send this message explicitly or by using the [**TreeView\_GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d872-108">參數</span><span class="sxs-lookup"><span data-stu-id="5d872-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d872-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d872-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5d872-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5d872-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5d872-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d872-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5d872-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5d872-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d872-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d872-113">Return value</span></span>

<span data-ttu-id="5d872-114">傳回縮排的量。</span><span class="sxs-lookup"><span data-stu-id="5d872-114">Returns the amount of indentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d872-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d872-115">Requirements</span></span>



| <span data-ttu-id="5d872-116">需求</span><span class="sxs-lookup"><span data-stu-id="5d872-116">Requirement</span></span> | <span data-ttu-id="5d872-117">值</span><span class="sxs-lookup"><span data-stu-id="5d872-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d872-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d872-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5d872-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d872-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d872-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d872-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5d872-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d872-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d872-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5d872-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d872-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d872-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






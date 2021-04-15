---
title: 'TVM_SORTCHILDRENCB 訊息 (Commctrl .h) '
description: 使用會比較專案的應用程式定義回呼函式，來排序樹狀檢視專案。 您可以使用 TreeView SortChildrenCB 宏明確地傳送此訊息 \_ 。
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- TVM_SORTCHILDRENCB message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466793"
---
# <a name="tvm_sortchildrencb-message"></a><span data-ttu-id="ec6fe-105">TVM \_ SORTCHILDRENCB 訊息</span><span class="sxs-lookup"><span data-stu-id="ec6fe-105">TVM\_SORTCHILDRENCB message</span></span>

<span data-ttu-id="ec6fe-106">使用會比較專案的應用程式定義回呼函式，來排序樹狀檢視專案。</span><span class="sxs-lookup"><span data-stu-id="ec6fe-106">Sorts tree-view items using an application-defined callback function that compares the items.</span></span> <span data-ttu-id="ec6fe-107">您可以使用 [**TreeView \_ SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ec6fe-107">You can send this message explicitly or by using the [**TreeView\_SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec6fe-108">參數</span><span class="sxs-lookup"><span data-stu-id="ec6fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec6fe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec6fe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec6fe-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="ec6fe-110">Reserved.</span></span> <span data-ttu-id="ec6fe-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ec6fe-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ec6fe-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec6fe-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec6fe-113">[**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ec6fe-113">Pointer to a [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) structure.</span></span> <span data-ttu-id="ec6fe-114">**LpfnCompare** 成員是應用程式定義的回呼函式的位址，每次需要比較兩個清單專案的相對順序時，就會在排序作業期間呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="ec6fe-114">The **lpfnCompare** member is the address of the application-defined callback function, which is called during the sort operation each time the relative order of two list items needs to be compared.</span></span> <span data-ttu-id="ec6fe-115">如需回呼函數的詳細資訊，請參閱 **TVSORTCB** 的描述。</span><span class="sxs-lookup"><span data-stu-id="ec6fe-115">For more information about the callback function, see the description of **TVSORTCB**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec6fe-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec6fe-116">Return value</span></span>

<span data-ttu-id="ec6fe-117">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ec6fe-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec6fe-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec6fe-118">Requirements</span></span>



| <span data-ttu-id="ec6fe-119">需求</span><span class="sxs-lookup"><span data-stu-id="ec6fe-119">Requirement</span></span> | <span data-ttu-id="ec6fe-120">值</span><span class="sxs-lookup"><span data-stu-id="ec6fe-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec6fe-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec6fe-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ec6fe-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec6fe-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec6fe-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec6fe-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ec6fe-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec6fe-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec6fe-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ec6fe-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec6fe-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec6fe-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: 'LVM_SETITEMINDEXSTATE 訊息 (Commctrl .h) '
description: 設定清單視圖專案的狀態。 明確地傳送此訊息，或使用 ListView \_ SetItemIndexState 宏。
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- LVM_SETITEMINDEXSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024855"
---
# <a name="lvm_setitemindexstate-message"></a><span data-ttu-id="89464-105">LVM \_ SETITEMINDEXSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="89464-105">LVM\_SETITEMINDEXSTATE message</span></span>

<span data-ttu-id="89464-106">設定清單視圖專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="89464-106">Sets the state of a list-view item.</span></span> <span data-ttu-id="89464-107">明確地傳送此訊息，或使用 [**ListView \_ SetItemIndexState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) 宏。</span><span class="sxs-lookup"><span data-stu-id="89464-107">Send this message explicitly or by using the [**ListView\_SetItemIndexState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="89464-108">參數</span><span class="sxs-lookup"><span data-stu-id="89464-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89464-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89464-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89464-110">專案之 [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="89464-110">A pointer to an [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the item.</span></span> <span data-ttu-id="89464-111">呼叫進程負責配置此結構及設定成員。</span><span class="sxs-lookup"><span data-stu-id="89464-111">The calling process is responsible for allocating this structure and setting the members.</span></span>

</dd> <dt>

<span data-ttu-id="89464-112">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89464-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89464-113">[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="89464-113">A pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="89464-114">呼叫進程負責為結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="89464-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="89464-115">將 **狀態** 成員設定為一或多個 (為 [清單視圖專案狀態](list-view-item-states.md) 旗標的位合) 。</span><span class="sxs-lookup"><span data-stu-id="89464-115">Set the **state** member to one or more (as a bitwise combination) of the [List-View Item States](list-view-item-states.md) flags.</span></span> <span data-ttu-id="89464-116">設定結構的 **stateMask** 成員，以表示 **狀態** 成員的有效位。</span><span class="sxs-lookup"><span data-stu-id="89464-116">Set the **stateMask** member of the structure to indicate the valid bits of the **state** member.</span></span> <span data-ttu-id="89464-117">如需詳細資訊，請參閱 **LVITEM** 結構的 **stateMask** 成員。</span><span class="sxs-lookup"><span data-stu-id="89464-117">For more information, see the **stateMask** member of the **LVITEM** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89464-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="89464-118">Return value</span></span>

<span data-ttu-id="89464-119">傳回下列其中一個 **HRESULT** 型別的值。</span><span class="sxs-lookup"><span data-stu-id="89464-119">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="89464-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="89464-120">Return code</span></span>                                                                                  | <span data-ttu-id="89464-121">Description</span><span class="sxs-lookup"><span data-stu-id="89464-121">Description</span></span>                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="89464-122"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="89464-122"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="89464-123">無法設定狀態。</span><span class="sxs-lookup"><span data-stu-id="89464-123">The state could not be set.</span></span><br/>                            |
| <dl> <span data-ttu-id="89464-124"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="89464-124"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="89464-125">清單視圖控制項尚未準備好進行操作。</span><span class="sxs-lookup"><span data-stu-id="89464-125">The list-view control was not ready for the operation.</span></span><br/> |
| <dl> <span data-ttu-id="89464-126"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="89464-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="89464-127">作業成功。</span><span class="sxs-lookup"><span data-stu-id="89464-127">The operation was successful.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="89464-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="89464-128">Requirements</span></span>



| <span data-ttu-id="89464-129">需求</span><span class="sxs-lookup"><span data-stu-id="89464-129">Requirement</span></span> | <span data-ttu-id="89464-130">值</span><span class="sxs-lookup"><span data-stu-id="89464-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89464-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89464-131">Minimum supported client</span></span><br/> | <span data-ttu-id="89464-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89464-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89464-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89464-133">Minimum supported server</span></span><br/> | <span data-ttu-id="89464-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89464-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89464-135">標頭</span><span class="sxs-lookup"><span data-stu-id="89464-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="89464-136"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="89464-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






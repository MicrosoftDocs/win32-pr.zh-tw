---
title: 'CBEM_GETITEM 訊息 (Commctrl .h) '
description: 取得指定之 ComboBoxEx 專案的專案資訊。
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- CBEM_GETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940bbf7aea8ec93dd0f808937d959477c964df96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967359"
---
# <a name="cbem_getitem-message"></a><span data-ttu-id="090b3-104">CBEM \_ GETITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="090b3-104">CBEM\_GETITEM message</span></span>

<span data-ttu-id="090b3-105">取得指定之 ComboBoxEx 專案的專案資訊。</span><span class="sxs-lookup"><span data-stu-id="090b3-105">Gets item information for a given ComboBoxEx item.</span></span>

## <a name="parameters"></a><span data-ttu-id="090b3-106">參數</span><span class="sxs-lookup"><span data-stu-id="090b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090b3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="090b3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="090b3-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="090b3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="090b3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="090b3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="090b3-110">[**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的指標，此結構會接收專案資訊。</span><span class="sxs-lookup"><span data-stu-id="090b3-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that receives the item information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090b3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="090b3-111">Return value</span></span>

<span data-ttu-id="090b3-112">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="090b3-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="090b3-113">備註</span><span class="sxs-lookup"><span data-stu-id="090b3-113">Remarks</span></span>

<span data-ttu-id="090b3-114">傳送訊息時，必須設定結構的 **iItem** 和 **mask** 成員，以表示目標專案的索引，以及要抓取的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="090b3-114">When the message is sent, the **iItem** and **mask** members of the structure must be set to indicate the index of the target item and the type of information to be retrieved.</span></span> <span data-ttu-id="090b3-115">其他成員則會視需要設定。</span><span class="sxs-lookup"><span data-stu-id="090b3-115">Other members are set as needed.</span></span> <span data-ttu-id="090b3-116">例如，若要取出文字，您必須 \_ 在 **mask** 中設定 CBEIF 文字旗標，並將值指派給 **cchTextMax**。</span><span class="sxs-lookup"><span data-stu-id="090b3-116">For example, to retrieve text, you must set the CBEIF\_TEXT flag in **mask**, and assign a value to **cchTextMax**.</span></span> <span data-ttu-id="090b3-117">將 **iItem** 成員設定為-1，將會抓取編輯控制項中顯示的專案。</span><span class="sxs-lookup"><span data-stu-id="090b3-117">Setting the **iItem** member to -1 will retrieve the item displayed in the edit control.</span></span>

<span data-ttu-id="090b3-118">如果在 \_ [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的 **MASK** 成員中設定 CBEIF 文字旗標，控制項可能會變更結構的 **pszText** 成員以指向新的文字，而不是以要求的文字填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="090b3-118">If the CBEIF\_TEXT flag is set in the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="090b3-119">應用程式不應假設文字一定會放在要求的緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="090b3-119">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="090b3-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="090b3-120">Requirements</span></span>



| <span data-ttu-id="090b3-121">需求</span><span class="sxs-lookup"><span data-stu-id="090b3-121">Requirement</span></span> | <span data-ttu-id="090b3-122">值</span><span class="sxs-lookup"><span data-stu-id="090b3-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="090b3-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="090b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="090b3-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="090b3-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="090b3-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="090b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="090b3-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="090b3-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="090b3-127">標頭</span><span class="sxs-lookup"><span data-stu-id="090b3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="090b3-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="090b3-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="090b3-129">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="090b3-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="090b3-130">**CBEM \_GETITEMW** (Unicode) 和 **CBEM \_ GETITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="090b3-130">**CBEM\_GETITEMW** (Unicode) and **CBEM\_GETITEMA** (ANSI)</span></span><br/>                 |



 

 






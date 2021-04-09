---
title: 'CBEM_SETITEM 訊息 (Commctrl .h) '
description: 設定 ComboBoxEx 控制項中專案的屬性。
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- CBEM_SETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686382"
---
# <a name="cbem_setitem-message"></a><span data-ttu-id="d7353-104">CBEM \_ SETITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="d7353-104">CBEM\_SETITEM message</span></span>

<span data-ttu-id="d7353-105">設定 ComboBoxEx 控制項中專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="d7353-105">Sets the attributes for an item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7353-106">參數</span><span class="sxs-lookup"><span data-stu-id="d7353-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7353-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7353-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d7353-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d7353-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d7353-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7353-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7353-110">[**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的指標，其中包含要設定的專案資訊。</span><span class="sxs-lookup"><span data-stu-id="d7353-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains the item information to be set.</span></span> <span data-ttu-id="d7353-111">傳送訊息時，必須設定結構的 **遮罩** 成員，以指出哪些屬性有效，且 **iItem** 成員必須指定要修改之專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="d7353-111">When the message is sent, the **mask** member of the structure must be set to indicate which attributes are valid and the **iItem** member must specify the zero-based index of the item to be modified.</span></span> <span data-ttu-id="d7353-112">將 **iItem** 成員設定為-1，將會修改編輯控制項中顯示的專案。</span><span class="sxs-lookup"><span data-stu-id="d7353-112">Setting the **iItem** member to -1 will modify the item displayed in the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7353-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7353-113">Return value</span></span>

<span data-ttu-id="d7353-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="d7353-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7353-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7353-115">Requirements</span></span>



| <span data-ttu-id="d7353-116">需求</span><span class="sxs-lookup"><span data-stu-id="d7353-116">Requirement</span></span> | <span data-ttu-id="d7353-117">值</span><span class="sxs-lookup"><span data-stu-id="d7353-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7353-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7353-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d7353-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7353-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7353-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7353-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d7353-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7353-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7353-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d7353-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7353-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7353-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d7353-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d7353-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d7353-125">**CBEM \_SETITEMW** (Unicode) 和 **CBEM \_ SETITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d7353-125">**CBEM\_SETITEMW** (Unicode) and **CBEM\_SETITEMA** (ANSI)</span></span><br/>                 |



 

 






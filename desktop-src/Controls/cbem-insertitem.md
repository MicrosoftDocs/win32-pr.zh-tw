---
title: 'CBEM_INSERTITEM 訊息 (Commctrl .h) '
description: 在 ComboBoxEx 控制項中插入新專案。
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- CBEM_INSERTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976977"
---
# <a name="cbem_insertitem-message"></a><span data-ttu-id="6fde3-104">CBEM \_ INSERTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="6fde3-104">CBEM\_INSERTITEM message</span></span>

<span data-ttu-id="6fde3-105">在 ComboBoxEx 控制項中插入新專案。</span><span class="sxs-lookup"><span data-stu-id="6fde3-105">Inserts a new item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6fde3-106">參數</span><span class="sxs-lookup"><span data-stu-id="6fde3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fde3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6fde3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6fde3-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6fde3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6fde3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fde3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fde3-110">[**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的指標，其中包含要插入之專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6fde3-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains information about the item to be inserted.</span></span> <span data-ttu-id="6fde3-111">傳送訊息時，必須設定 **iItem** 成員，以表示要插入專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="6fde3-111">When the message is sent, the **iItem** member must be set to indicate the zero-based index at which to insert the item.</span></span> <span data-ttu-id="6fde3-112">若要在清單結尾插入專案，請將 **iItem** 成員設定為-1。</span><span class="sxs-lookup"><span data-stu-id="6fde3-112">To insert an item at the end of the list, set the **iItem** member to -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fde3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6fde3-113">Return value</span></span>

<span data-ttu-id="6fde3-114">如果成功，則傳回插入新專案的索引，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="6fde3-114">Returns the index at which the new item was inserted if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fde3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6fde3-115">Requirements</span></span>



| <span data-ttu-id="6fde3-116">需求</span><span class="sxs-lookup"><span data-stu-id="6fde3-116">Requirement</span></span> | <span data-ttu-id="6fde3-117">值</span><span class="sxs-lookup"><span data-stu-id="6fde3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fde3-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6fde3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6fde3-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6fde3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6fde3-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6fde3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6fde3-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6fde3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6fde3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6fde3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fde3-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6fde3-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6fde3-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="6fde3-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6fde3-125">**CBEM \_INSERTITEMW** (Unicode) 和 **CBEM \_ INSERTITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="6fde3-125">**CBEM\_INSERTITEMW** (Unicode) and **CBEM\_INSERTITEMA** (ANSI)</span></span><br/>           |



 

 






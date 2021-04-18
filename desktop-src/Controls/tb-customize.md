---
title: 'TB_CUSTOMIZE 訊息 (Commctrl .h) '
description: 顯示 [自訂工具列] 對話方塊。
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- TB_CUSTOMIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965538"
---
# <a name="tb_customize-message"></a><span data-ttu-id="e55d0-104">TB \_ 自訂訊息</span><span class="sxs-lookup"><span data-stu-id="e55d0-104">TB\_CUSTOMIZE message</span></span>

<span data-ttu-id="e55d0-105">顯示 [ **自訂工具列** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e55d0-105">Displays the **Customize Toolbar** dialog box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e55d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="e55d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e55d0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e55d0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e55d0-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e55d0-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e55d0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e55d0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e55d0-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e55d0-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e55d0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e55d0-111">Return value</span></span>

<span data-ttu-id="e55d0-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e55d0-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e55d0-113">備註</span><span class="sxs-lookup"><span data-stu-id="e55d0-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e55d0-114">工具列必須處理 [TBN \_ QUERYINSERT](tbn-queryinsert.md) 和 [TBN \_ QUERYDELETE](tbn-querydelete.md) 通知，才能顯示 [ **自訂工具列** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e55d0-114">The toolbar must handle the [TBN\_QUERYINSERT](tbn-queryinsert.md) and [TBN\_QUERYDELETE](tbn-querydelete.md) notifications for the **Customize Toolbar** dialog box to appear.</span></span> <span data-ttu-id="e55d0-115">如果工具列沒有處理這些通知，則 **TB \_ 自訂** 不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="e55d0-115">If the toolbar does not handle those notifications, **TB\_CUSTOMIZE** has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e55d0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e55d0-116">Requirements</span></span>



| <span data-ttu-id="e55d0-117">需求</span><span class="sxs-lookup"><span data-stu-id="e55d0-117">Requirement</span></span> | <span data-ttu-id="e55d0-118">值</span><span class="sxs-lookup"><span data-stu-id="e55d0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e55d0-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e55d0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e55d0-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e55d0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e55d0-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e55d0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e55d0-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e55d0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e55d0-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e55d0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e55d0-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e55d0-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






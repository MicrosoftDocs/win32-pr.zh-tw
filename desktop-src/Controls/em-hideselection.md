---
title: 'EM_HIDESELECTION 訊息 (Richedit .h) '
description: EM \_ HIDESELECTION 訊息會隱藏或顯示在 rich edit 控制項中的選取專案。
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- EM_HIDESELECTION message Windows 控制項
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933988"
---
# <a name="em_hideselection-message"></a><span data-ttu-id="7130a-104">EM \_ HIDESELECTION 訊息</span><span class="sxs-lookup"><span data-stu-id="7130a-104">EM\_HIDESELECTION message</span></span>

<span data-ttu-id="7130a-105">**EM \_ HIDESELECTION** 訊息會隱藏或顯示在 rich edit 控制項中的選取專案。</span><span class="sxs-lookup"><span data-stu-id="7130a-105">The **EM\_HIDESELECTION** message hides or shows the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7130a-106">參數</span><span class="sxs-lookup"><span data-stu-id="7130a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7130a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7130a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7130a-108">指定是否要隱藏或顯示選取範圍的值。</span><span class="sxs-lookup"><span data-stu-id="7130a-108">Value specifying whether to hide or show the selection.</span></span> <span data-ttu-id="7130a-109">如果此參數為零，則會顯示選取範圍。</span><span class="sxs-lookup"><span data-stu-id="7130a-109">If this parameter is zero, the selection is shown.</span></span> <span data-ttu-id="7130a-110">否則，就會隱藏選取範圍。</span><span class="sxs-lookup"><span data-stu-id="7130a-110">Otherwise, the selection is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="7130a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7130a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7130a-112">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="7130a-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7130a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7130a-113">Return value</span></span>

<span data-ttu-id="7130a-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7130a-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7130a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7130a-115">Requirements</span></span>



| <span data-ttu-id="7130a-116">需求</span><span class="sxs-lookup"><span data-stu-id="7130a-116">Requirement</span></span> | <span data-ttu-id="7130a-117">值</span><span class="sxs-lookup"><span data-stu-id="7130a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7130a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7130a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7130a-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7130a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7130a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7130a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7130a-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7130a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7130a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7130a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7130a-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="7130a-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 






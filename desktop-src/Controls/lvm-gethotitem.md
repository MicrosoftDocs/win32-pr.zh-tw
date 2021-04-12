---
title: 'LVM_GETHOTITEM 訊息 (Commctrl .h) '
description: 抓取熱專案的索引。 您可以明確地傳送此訊息，或使用 ListView \_ GetHotItem 宏。
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- LVM_GETHOTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c7bbfb845518eb40b55556df5294d59cff3d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105515"
---
# <a name="lvm_gethotitem-message"></a><span data-ttu-id="b8bfe-105">LVM \_ GETHOTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="b8bfe-105">LVM\_GETHOTITEM message</span></span>

<span data-ttu-id="b8bfe-106">抓取熱專案的索引。</span><span class="sxs-lookup"><span data-stu-id="b8bfe-106">Retrieves the index of the hot item.</span></span> <span data-ttu-id="b8bfe-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) 宏。</span><span class="sxs-lookup"><span data-stu-id="b8bfe-107">You can send this message explicitly or use the [**ListView\_GetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8bfe-108">參數</span><span class="sxs-lookup"><span data-stu-id="b8bfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8bfe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8bfe-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b8bfe-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b8bfe-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b8bfe-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8bfe-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b8bfe-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b8bfe-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8bfe-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8bfe-113">Return value</span></span>

<span data-ttu-id="b8bfe-114">傳回熱專案的索引。</span><span class="sxs-lookup"><span data-stu-id="b8bfe-114">Returns the index of the item that is hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8bfe-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8bfe-115">Requirements</span></span>



| <span data-ttu-id="b8bfe-116">需求</span><span class="sxs-lookup"><span data-stu-id="b8bfe-116">Requirement</span></span> | <span data-ttu-id="b8bfe-117">值</span><span class="sxs-lookup"><span data-stu-id="b8bfe-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8bfe-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8bfe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8bfe-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8bfe-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8bfe-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8bfe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8bfe-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8bfe-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8bfe-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b8bfe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8bfe-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8bfe-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






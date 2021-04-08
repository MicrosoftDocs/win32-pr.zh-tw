---
title: 'LVM_GETITEMCOUNT 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項中的專案數。 您可以明確地傳送此訊息，或使用 ListView \_ GetItemCount 宏來傳送。
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- LVM_GETITEMCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2791440c7285d054eca0d2945086d06e3c35a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686280"
---
# <a name="lvm_getitemcount-message"></a><span data-ttu-id="9466f-105">LVM \_ GETITEMCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="9466f-105">LVM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="9466f-106">抓取清單視圖控制項中的專案數。</span><span class="sxs-lookup"><span data-stu-id="9466f-106">Retrieves the number of items in a list-view control.</span></span> <span data-ttu-id="9466f-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="9466f-107">You can send this message explicitly or by using the [**ListView\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9466f-108">參數</span><span class="sxs-lookup"><span data-stu-id="9466f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9466f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9466f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9466f-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9466f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9466f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9466f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9466f-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9466f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9466f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9466f-113">Return value</span></span>

<span data-ttu-id="9466f-114">傳回專案的數目。</span><span class="sxs-lookup"><span data-stu-id="9466f-114">Returns the number of items.</span></span>

## <a name="requirements"></a><span data-ttu-id="9466f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9466f-115">Requirements</span></span>



| <span data-ttu-id="9466f-116">需求</span><span class="sxs-lookup"><span data-stu-id="9466f-116">Requirement</span></span> | <span data-ttu-id="9466f-117">值</span><span class="sxs-lookup"><span data-stu-id="9466f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9466f-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9466f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9466f-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9466f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9466f-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9466f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9466f-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9466f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9466f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9466f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9466f-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9466f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






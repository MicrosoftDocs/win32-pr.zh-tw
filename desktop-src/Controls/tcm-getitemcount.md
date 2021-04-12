---
title: 'TCM_GETITEMCOUNT 訊息 (Commctrl .h) '
description: 抓取索引標籤控制項中的索引標籤數目。 您可以使用 TabCtrl GetItemCount 宏明確地傳送此訊息 \_ 。
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- TCM_GETITEMCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d638a9be81581605b978695c8504f538967c77f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105743"
---
# <a name="tcm_getitemcount-message"></a><span data-ttu-id="349e1-105">TCM \_ GETITEMCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="349e1-105">TCM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="349e1-106">抓取索引標籤控制項中的索引標籤數目。</span><span class="sxs-lookup"><span data-stu-id="349e1-106">Retrieves the number of tabs in the tab control.</span></span> <span data-ttu-id="349e1-107">您可以使用 [**TabCtrl \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="349e1-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="349e1-108">參數</span><span class="sxs-lookup"><span data-stu-id="349e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="349e1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="349e1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="349e1-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="349e1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="349e1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="349e1-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="349e1-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="349e1-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="349e1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="349e1-113">Return value</span></span>

<span data-ttu-id="349e1-114">如果成功，則傳回專案的數目，否則為零。</span><span class="sxs-lookup"><span data-stu-id="349e1-114">Returns the number of items if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="349e1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="349e1-115">Requirements</span></span>



| <span data-ttu-id="349e1-116">需求</span><span class="sxs-lookup"><span data-stu-id="349e1-116">Requirement</span></span> | <span data-ttu-id="349e1-117">值</span><span class="sxs-lookup"><span data-stu-id="349e1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="349e1-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="349e1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="349e1-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="349e1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="349e1-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="349e1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="349e1-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="349e1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="349e1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="349e1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="349e1-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="349e1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






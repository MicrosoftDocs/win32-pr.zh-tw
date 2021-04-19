---
title: 'TCM_SETMINTABWIDTH 訊息 (Commctrl .h) '
description: 設定索引標籤控制項中專案的最小寬度。 您可以使用 TabCtrl SetMinTabWidth 宏明確地傳送此訊息 \_ 。
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- TCM_SETMINTABWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969557"
---
# <a name="tcm_setmintabwidth-message"></a><span data-ttu-id="d79cd-105">TCM \_ SETMINTABWIDTH 訊息</span><span class="sxs-lookup"><span data-stu-id="d79cd-105">TCM\_SETMINTABWIDTH message</span></span>

<span data-ttu-id="d79cd-106">設定索引標籤控制項中專案的最小寬度。</span><span class="sxs-lookup"><span data-stu-id="d79cd-106">Sets the minimum width of items in a tab control.</span></span> <span data-ttu-id="d79cd-107">您可以使用 [**TabCtrl \_ SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d79cd-107">You can send this message explicitly or by using the [**TabCtrl\_SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d79cd-108">參數</span><span class="sxs-lookup"><span data-stu-id="d79cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d79cd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d79cd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d79cd-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d79cd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d79cd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d79cd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d79cd-112">要針對索引標籤控制項專案設定的最小寬度。</span><span class="sxs-lookup"><span data-stu-id="d79cd-112">Minimum width to be set for a tab control item.</span></span> <span data-ttu-id="d79cd-113">如果此參數設定為-1，此控制項將會使用預設的定位鍵寬度。</span><span class="sxs-lookup"><span data-stu-id="d79cd-113">If this parameter is set to -1, the control will use the default tab width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d79cd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d79cd-114">Return value</span></span>

<span data-ttu-id="d79cd-115">傳回 INT 值，表示先前的最小索引標籤寬度。</span><span class="sxs-lookup"><span data-stu-id="d79cd-115">Returns an INT value that represents the previous minimum tab width.</span></span>

## <a name="requirements"></a><span data-ttu-id="d79cd-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d79cd-116">Requirements</span></span>



| <span data-ttu-id="d79cd-117">需求</span><span class="sxs-lookup"><span data-stu-id="d79cd-117">Requirement</span></span> | <span data-ttu-id="d79cd-118">值</span><span class="sxs-lookup"><span data-stu-id="d79cd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d79cd-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d79cd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d79cd-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d79cd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d79cd-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d79cd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d79cd-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d79cd-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d79cd-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d79cd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d79cd-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d79cd-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






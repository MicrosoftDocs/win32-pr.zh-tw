---
title: 'TCM_GETCURSEL 訊息 (Commctrl .h) '
description: 決定目前在索引標籤控制項中選取的索引標籤。 您可以使用 TabCtrl GetCurSel 宏明確地傳送此訊息 \_ 。
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- TCM_GETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969813"
---
# <a name="tcm_getcursel-message"></a><span data-ttu-id="9b7b1-105">TCM \_ GETCURSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="9b7b1-105">TCM\_GETCURSEL message</span></span>

<span data-ttu-id="9b7b1-106">決定目前在索引標籤控制項中選取的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="9b7b1-106">Determines the currently selected tab in a tab control.</span></span> <span data-ttu-id="9b7b1-107">您可以使用 [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="9b7b1-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b7b1-108">參數</span><span class="sxs-lookup"><span data-stu-id="9b7b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b7b1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b7b1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9b7b1-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9b7b1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9b7b1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b7b1-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9b7b1-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9b7b1-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b7b1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b7b1-113">Return value</span></span>

<span data-ttu-id="9b7b1-114">如果成功，則傳回所選索引標籤的索引; 如果未選取任何索引標籤，則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="9b7b1-114">Returns the index of the selected tab if successful, or -1 if no tab is selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b7b1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b7b1-115">Requirements</span></span>



| <span data-ttu-id="9b7b1-116">需求</span><span class="sxs-lookup"><span data-stu-id="9b7b1-116">Requirement</span></span> | <span data-ttu-id="9b7b1-117">值</span><span class="sxs-lookup"><span data-stu-id="9b7b1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b7b1-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b7b1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9b7b1-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b7b1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b7b1-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b7b1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9b7b1-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b7b1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b7b1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9b7b1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b7b1-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b7b1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: 'TCM_HITTEST 訊息 (Commctrl .h) '
description: 判斷哪一個索引標籤（如果有的話）位於指定的畫面位置上。 您可以使用 TabCtrl System.windows.media.visualtreehelper.hittest 宏明確地傳送此訊息 \_ 。
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- TCM_HITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970446"
---
# <a name="tcm_hittest-message"></a><span data-ttu-id="1e7f8-105">TCM \_ system.windows.media.visualtreehelper.hittest 訊息</span><span class="sxs-lookup"><span data-stu-id="1e7f8-105">TCM\_HITTEST message</span></span>

<span data-ttu-id="1e7f8-106">判斷哪一個索引標籤（如果有的話）位於指定的畫面位置上。</span><span class="sxs-lookup"><span data-stu-id="1e7f8-106">Determines which tab, if any, is at a specified screen position.</span></span> <span data-ttu-id="1e7f8-107">您可以使用 [**TabCtrl \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1e7f8-107">You can send this message explicitly or by using the [**TabCtrl\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e7f8-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e7f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e7f8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e7f8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1e7f8-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1e7f8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1e7f8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e7f8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e7f8-112">[**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo)結構的指標，指定要測試的螢幕位置。</span><span class="sxs-lookup"><span data-stu-id="1e7f8-112">Pointer to a [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) structure that specifies the screen position to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e7f8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e7f8-113">Return value</span></span>

<span data-ttu-id="1e7f8-114">傳回索引標籤的索引，如果沒有索引標籤位於指定的位置，則為-1。</span><span class="sxs-lookup"><span data-stu-id="1e7f8-114">Returns the index of the tab, or -1 if no tab is at the specified position.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e7f8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e7f8-115">Requirements</span></span>



| <span data-ttu-id="1e7f8-116">需求</span><span class="sxs-lookup"><span data-stu-id="1e7f8-116">Requirement</span></span> | <span data-ttu-id="1e7f8-117">值</span><span class="sxs-lookup"><span data-stu-id="1e7f8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e7f8-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e7f8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1e7f8-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e7f8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e7f8-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e7f8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1e7f8-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e7f8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e7f8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1e7f8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e7f8-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e7f8-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






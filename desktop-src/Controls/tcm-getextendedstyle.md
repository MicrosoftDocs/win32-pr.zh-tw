---
title: 'TCM_GETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 抓取目前用於索引標籤控制項的延伸樣式。 您可以使用 TabCtrl GetExtendedStyle 宏明確地傳送此訊息 \_ 。
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- TCM_GETEXTENDEDSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934947"
---
# <a name="tcm_getextendedstyle-message"></a><span data-ttu-id="af0ca-105">TCM \_ GETEXTENDEDSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="af0ca-105">TCM\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="af0ca-106">抓取目前用於索引標籤控制項的延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="af0ca-106">Retrieves the extended styles that are currently in use for the tab control.</span></span> <span data-ttu-id="af0ca-107">您可以使用 [**TabCtrl \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="af0ca-107">You can send this message explicitly or by using the [**TabCtrl\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="af0ca-108">參數</span><span class="sxs-lookup"><span data-stu-id="af0ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af0ca-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af0ca-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="af0ca-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="af0ca-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="af0ca-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af0ca-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="af0ca-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="af0ca-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af0ca-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="af0ca-113">Return value</span></span>

<span data-ttu-id="af0ca-114">傳回 **DWORD** 值，表示目前用於索引標籤控制項的延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="af0ca-114">Returns a **DWORD** value that represents the extended styles currently in use for the tab control.</span></span> <span data-ttu-id="af0ca-115">此值為索引標籤控制項 [擴充樣式](tab-control-extended-styles.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="af0ca-115">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af0ca-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="af0ca-116">Requirements</span></span>



| <span data-ttu-id="af0ca-117">需求</span><span class="sxs-lookup"><span data-stu-id="af0ca-117">Requirement</span></span> | <span data-ttu-id="af0ca-118">值</span><span class="sxs-lookup"><span data-stu-id="af0ca-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af0ca-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af0ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="af0ca-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af0ca-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af0ca-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af0ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="af0ca-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af0ca-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af0ca-123">標頭</span><span class="sxs-lookup"><span data-stu-id="af0ca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="af0ca-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="af0ca-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af0ca-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af0ca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af0ca-126">**TCM \_ SETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="af0ca-126">**TCM\_SETEXTENDEDSTYLE**</span></span>](tcm-setextendedstyle.md)
</dt> </dl>

 

 






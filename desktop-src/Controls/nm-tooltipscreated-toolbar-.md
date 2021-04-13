---
title: 'NM_TOOLTIPSCREATED (工具列) 通知碼 (Commctrl) '
description: 通知工具列的父視窗，工具列已建立工具提示控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- NM_TOOLTIPSCREATED (工具列) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464872"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a><span data-ttu-id="180a4-105">NM \_ TOOLTIPSCREATED (工具列) 通知碼</span><span class="sxs-lookup"><span data-stu-id="180a4-105">NM\_TOOLTIPSCREATED (toolbar) notification code</span></span>

<span data-ttu-id="180a4-106">通知工具列的父視窗，工具列已建立工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="180a4-106">Notifies a toolbar's parent window that the toolbar has created a tooltip control.</span></span> <span data-ttu-id="180a4-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="180a4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="180a4-108">參數</span><span class="sxs-lookup"><span data-stu-id="180a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="180a4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="180a4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="180a4-110">[**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="180a4-110">Pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="180a4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="180a4-111">Return value</span></span>

<span data-ttu-id="180a4-112">Toolbar 控制項會忽略此通知碼的傳回值。</span><span class="sxs-lookup"><span data-stu-id="180a4-112">The toolbar control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="180a4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="180a4-113">Requirements</span></span>



| <span data-ttu-id="180a4-114">需求</span><span class="sxs-lookup"><span data-stu-id="180a4-114">Requirement</span></span> | <span data-ttu-id="180a4-115">值</span><span class="sxs-lookup"><span data-stu-id="180a4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="180a4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="180a4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="180a4-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="180a4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="180a4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="180a4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="180a4-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="180a4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="180a4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="180a4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="180a4-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="180a4-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






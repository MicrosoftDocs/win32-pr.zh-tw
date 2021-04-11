---
title: 'HDN_ENDFILTEREDIT (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，篩選編輯已結束。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d3832875-4cde-4d8a-b3a4-a8dae0742c56
keywords:
- HDN_ENDFILTEREDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ENDFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a557278598600f1bd11ebfbe791691de954a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686683"
---
# <a name="hdn_endfilteredit-notification-code"></a><span data-ttu-id="6c8d8-105">HDN \_ ENDFILTEREDIT 通知碼</span><span class="sxs-lookup"><span data-stu-id="6c8d8-105">HDN\_ENDFILTEREDIT notification code</span></span>

<span data-ttu-id="6c8d8-106">通知標題控制項的父視窗，篩選編輯已結束。</span><span class="sxs-lookup"><span data-stu-id="6c8d8-106">Notifies a header control's parent window that a filter edit has ended.</span></span> <span data-ttu-id="6c8d8-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="6c8d8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ENDFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6c8d8-108">參數</span><span class="sxs-lookup"><span data-stu-id="6c8d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c8d8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c8d8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c8d8-110">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含正在編輯之篩選的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="6c8d8-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the filter that is being edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c8d8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c8d8-111">Return value</span></span>

<span data-ttu-id="6c8d8-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6c8d8-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8d8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c8d8-113">Requirements</span></span>



| <span data-ttu-id="6c8d8-114">需求</span><span class="sxs-lookup"><span data-stu-id="6c8d8-114">Requirement</span></span> | <span data-ttu-id="6c8d8-115">值</span><span class="sxs-lookup"><span data-stu-id="6c8d8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8d8-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c8d8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c8d8-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c8d8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c8d8-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c8d8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c8d8-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c8d8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c8d8-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6c8d8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c8d8-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c8d8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






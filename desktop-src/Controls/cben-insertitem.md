---
title: 'CBEN_INSERTITEM (Commctrl 的通知碼) '
description: 在控制項中插入新專案時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- CBEN_INSERTITEM 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ccd05ea75015479ef32415d920bbe639664ac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686587"
---
# <a name="cben_insertitem-notification-code"></a><span data-ttu-id="ce821-105">CBEN \_ INSERTITEM 通知碼</span><span class="sxs-lookup"><span data-stu-id="ce821-105">CBEN\_INSERTITEM notification code</span></span>

<span data-ttu-id="ce821-106">在控制項中插入新專案時傳送。</span><span class="sxs-lookup"><span data-stu-id="ce821-106">Sent when a new item has been inserted in the control.</span></span> <span data-ttu-id="ce821-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="ce821-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ce821-108">參數</span><span class="sxs-lookup"><span data-stu-id="ce821-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce821-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce821-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce821-110">[**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)結構的指標，其中包含通知碼和已插入之專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ce821-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure containing information about the notification code and the item that was inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce821-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce821-111">Return value</span></span>

<span data-ttu-id="ce821-112">處理此通知程式碼的應用程式必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="ce821-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce821-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce821-113">Requirements</span></span>



| <span data-ttu-id="ce821-114">需求</span><span class="sxs-lookup"><span data-stu-id="ce821-114">Requirement</span></span> | <span data-ttu-id="ce821-115">值</span><span class="sxs-lookup"><span data-stu-id="ce821-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce821-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce821-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ce821-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce821-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce821-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce821-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ce821-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce821-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce821-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ce821-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce821-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce821-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






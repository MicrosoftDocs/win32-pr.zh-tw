---
title: 'CBEN_DELETEITEM (Commctrl 的通知碼) '
description: 在刪除專案時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 8b0d03ff-57fa-44dc-ab3e-05089b876e3c
keywords:
- CBEN_DELETEITEM 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBEN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c7ca7329898c9dd0c6bba76cba9d3524b017e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844196"
---
# <a name="cben_deleteitem-notification-code"></a><span data-ttu-id="56b26-105">CBEN \_ DELETEITEM 通知碼</span><span class="sxs-lookup"><span data-stu-id="56b26-105">CBEN\_DELETEITEM notification code</span></span>

<span data-ttu-id="56b26-106">在刪除專案時傳送。</span><span class="sxs-lookup"><span data-stu-id="56b26-106">Sent when an item has been deleted.</span></span> <span data-ttu-id="56b26-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="56b26-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DELETEITEM

    pCBEx = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="56b26-108">參數</span><span class="sxs-lookup"><span data-stu-id="56b26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56b26-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56b26-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56b26-110">[**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)結構的指標，其中包含通知碼和已刪除專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="56b26-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code and the deleted item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56b26-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="56b26-111">Return value</span></span>

<span data-ttu-id="56b26-112">處理此通知程式碼的應用程式必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="56b26-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="56b26-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="56b26-113">Requirements</span></span>



| <span data-ttu-id="56b26-114">需求</span><span class="sxs-lookup"><span data-stu-id="56b26-114">Requirement</span></span> | <span data-ttu-id="56b26-115">值</span><span class="sxs-lookup"><span data-stu-id="56b26-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56b26-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56b26-116">Minimum supported client</span></span><br/> | <span data-ttu-id="56b26-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56b26-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56b26-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56b26-118">Minimum supported server</span></span><br/> | <span data-ttu-id="56b26-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56b26-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56b26-120">標頭</span><span class="sxs-lookup"><span data-stu-id="56b26-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="56b26-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="56b26-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






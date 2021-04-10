---
title: 'HDN_ITEMKEYDOWN (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，已選取某個專案的按鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- HDN_ITEMKEYDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025481"
---
# <a name="hdn_itemkeydown-notification-code"></a><span data-ttu-id="16b7d-105">HDN \_ ITEMKEYDOWN 通知碼</span><span class="sxs-lookup"><span data-stu-id="16b7d-105">HDN\_ITEMKEYDOWN notification code</span></span>

<span data-ttu-id="16b7d-106">通知標題控制項的父視窗，已選取某個專案的按鍵。</span><span class="sxs-lookup"><span data-stu-id="16b7d-106">Notifies a header control's parent window that a key has been pressed with an item selected.</span></span> <span data-ttu-id="16b7d-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="16b7d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="16b7d-108">參數</span><span class="sxs-lookup"><span data-stu-id="16b7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b7d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16b7d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16b7d-110">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含所按下之索引鍵的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="16b7d-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16b7d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="16b7d-111">Return value</span></span>

<span data-ttu-id="16b7d-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="16b7d-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="16b7d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="16b7d-113">Requirements</span></span>



| <span data-ttu-id="16b7d-114">需求</span><span class="sxs-lookup"><span data-stu-id="16b7d-114">Requirement</span></span> | <span data-ttu-id="16b7d-115">值</span><span class="sxs-lookup"><span data-stu-id="16b7d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16b7d-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16b7d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="16b7d-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16b7d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16b7d-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16b7d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="16b7d-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16b7d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16b7d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="16b7d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="16b7d-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="16b7d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: 'HDN_ITEMDBLCLICK (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，使用者按兩下控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。 只有設定為 HDS 按鈕樣式的標題控制項才會 \_ 傳送此通知碼。
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e61117303ecc478a998da8799867988dbc1ca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187310"
---
# <a name="hdn_itemdblclick-notification-code"></a><span data-ttu-id="f42e8-106">HDN \_ ITEMDBLCLICK 通知碼</span><span class="sxs-lookup"><span data-stu-id="f42e8-106">HDN\_ITEMDBLCLICK notification code</span></span>

<span data-ttu-id="f42e8-107">通知標題控制項的父視窗，使用者按兩下控制項。</span><span class="sxs-lookup"><span data-stu-id="f42e8-107">Notifies a header control's parent window that the user double-clicked the control.</span></span> <span data-ttu-id="f42e8-108">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="f42e8-108">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="f42e8-109">只有設定為 [**HDS \_ 按鈕**](header-control-styles.md) 樣式的標題控制項才會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="f42e8-109">Only header controls that are set to the [**HDS\_BUTTONS**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f42e8-110">參數</span><span class="sxs-lookup"><span data-stu-id="f42e8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f42e8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f42e8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f42e8-112">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f42e8-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f42e8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f42e8-113">Return value</span></span>

<span data-ttu-id="f42e8-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="f42e8-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f42e8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f42e8-115">Requirements</span></span>



| <span data-ttu-id="f42e8-116">需求</span><span class="sxs-lookup"><span data-stu-id="f42e8-116">Requirement</span></span> | <span data-ttu-id="f42e8-117">值</span><span class="sxs-lookup"><span data-stu-id="f42e8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f42e8-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f42e8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f42e8-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f42e8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f42e8-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f42e8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f42e8-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f42e8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f42e8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f42e8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f42e8-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f42e8-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f42e8-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="f42e8-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f42e8-125">**HDN \_ITEMDBLCLICKW** (Unicode) 和 **HDN \_ ITEMDBLCLICKA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="f42e8-125">**HDN\_ITEMDBLCLICKW** (Unicode) and **HDN\_ITEMDBLCLICKA** (ANSI)</span></span><br/>         |



 

 






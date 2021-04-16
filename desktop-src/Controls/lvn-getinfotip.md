---
title: 'LVN_GETINFOTIP (Commctrl 的通知碼) '
description: 由大型圖示視圖清單-view 控制項（具有 LVS) EX 提示的 \_ \_ 延伸樣式）傳送。
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509494"
---
# <a name="lvn_getinfotip-notification-code"></a><span data-ttu-id="09c9c-104">LVN \_ GETINFOTIP 通知碼</span><span class="sxs-lookup"><span data-stu-id="09c9c-104">LVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="09c9c-105">由大型圖示視圖清單-view 控制項（具有 [**lvs) \_ EX \_**](extended-list-view-styles.md) 提示的延伸樣式）傳送。</span><span class="sxs-lookup"><span data-stu-id="09c9c-105">Sent by a large icon view list-view control that has the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="09c9c-106">當清單視圖控制項要求要顯示在工具提示中的其他文字資訊時，就會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="09c9c-106">This notification code is sent when the list-view control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="09c9c-107">它是以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="09c9c-107">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a><span data-ttu-id="09c9c-108">參數</span><span class="sxs-lookup"><span data-stu-id="09c9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09c9c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09c9c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09c9c-110">[**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="09c9c-110">Pointer to an [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09c9c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="09c9c-111">Return value</span></span>

<span data-ttu-id="09c9c-112">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="09c9c-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="09c9c-113">備註</span><span class="sxs-lookup"><span data-stu-id="09c9c-113">Remarks</span></span>

<span data-ttu-id="09c9c-114">此通知碼只會由具有 [**lvs) \_ EX \_**](extended-list-view-styles.md) 提示擴充樣式的清單視圖控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="09c9c-114">This notification code is only sent by list-view controls that have the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="09c9c-115">LVN \_ GETINFOTIP 通知碼只會針對子項0傳送。</span><span class="sxs-lookup"><span data-stu-id="09c9c-115">The LVN\_GETINFOTIP notification code is sent only for subitem 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="09c9c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="09c9c-116">Requirements</span></span>



| <span data-ttu-id="09c9c-117">需求</span><span class="sxs-lookup"><span data-stu-id="09c9c-117">Requirement</span></span> | <span data-ttu-id="09c9c-118">值</span><span class="sxs-lookup"><span data-stu-id="09c9c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09c9c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09c9c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="09c9c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09c9c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09c9c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09c9c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="09c9c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09c9c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09c9c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="09c9c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="09c9c-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="09c9c-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="09c9c-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="09c9c-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="09c9c-126">**LVN \_GETINFOTIPW** (Unicode) 和 **LVN \_ GETINFOTIPA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="09c9c-126">**LVN\_GETINFOTIPW** (Unicode) and **LVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 






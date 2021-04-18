---
title: 'HDN_ITEMSTATEICONCLICK 訊息 (Commctrl .h) '
description: 通知標題控制項的父視窗，使用者按一下專案的狀態圖示。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- HDN_ITEMSTATEICONCLICK message Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e5e162b78c829e60494f6e8ff81af3ca97eee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466937"
---
# <a name="hdn_itemstateiconclick-message"></a><span data-ttu-id="aefe6-105">HDN \_ ITEMSTATEICONCLICK 訊息</span><span class="sxs-lookup"><span data-stu-id="aefe6-105">HDN\_ITEMSTATEICONCLICK message</span></span>

<span data-ttu-id="aefe6-106">通知標題控制項的父視窗，使用者按一下專案的狀態圖示。</span><span class="sxs-lookup"><span data-stu-id="aefe6-106">Notifies a header control's parent window that the user clicked an item's state icon.</span></span> <span data-ttu-id="aefe6-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="aefe6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="aefe6-108">參數</span><span class="sxs-lookup"><span data-stu-id="aefe6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aefe6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aefe6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aefe6-110">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含有關已按一下之狀態圖示的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="aefe6-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the state icon that was clicked on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aefe6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="aefe6-111">Return value</span></span>

<span data-ttu-id="aefe6-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="aefe6-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aefe6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="aefe6-113">Requirements</span></span>



| <span data-ttu-id="aefe6-114">需求</span><span class="sxs-lookup"><span data-stu-id="aefe6-114">Requirement</span></span> | <span data-ttu-id="aefe6-115">值</span><span class="sxs-lookup"><span data-stu-id="aefe6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aefe6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aefe6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aefe6-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aefe6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aefe6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aefe6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aefe6-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aefe6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aefe6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="aefe6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aefe6-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="aefe6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






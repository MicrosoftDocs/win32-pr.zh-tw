---
title: 'HDN_ITEMCHANGED (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，標題專案的屬性已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ab707010-8ed2-4575-8233-8a1f5656e498
keywords:
- HDN_ITEMCHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGED
- HDN_ITEMCHANGEDA
- HDN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67157ff7f775c124236b7a77a1051b7644758c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024668"
---
# <a name="hdn_itemchanged-notification-code"></a><span data-ttu-id="3e38c-105">HDN \_ ITEMCHANGED 通知碼</span><span class="sxs-lookup"><span data-stu-id="3e38c-105">HDN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="3e38c-106">通知標題控制項的父視窗，標題專案的屬性已變更。</span><span class="sxs-lookup"><span data-stu-id="3e38c-106">Notifies a header control's parent window that the attributes of a header item have changed.</span></span> <span data-ttu-id="3e38c-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="3e38c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGED

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3e38c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3e38c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e38c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e38c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e38c-110">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項的相關資訊，包括已變更的屬性。</span><span class="sxs-lookup"><span data-stu-id="3e38c-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control, including the attributes that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e38c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e38c-111">Return value</span></span>

<span data-ttu-id="3e38c-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="3e38c-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e38c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e38c-113">Requirements</span></span>



| <span data-ttu-id="3e38c-114">需求</span><span class="sxs-lookup"><span data-stu-id="3e38c-114">Requirement</span></span> | <span data-ttu-id="3e38c-115">值</span><span class="sxs-lookup"><span data-stu-id="3e38c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e38c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e38c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3e38c-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e38c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e38c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e38c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3e38c-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e38c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e38c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3e38c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e38c-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e38c-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3e38c-122">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="3e38c-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3e38c-123">**HDN \_ITEMCHANGEDW** (Unicode) 和 **HDN \_ ITEMCHANGEDA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="3e38c-123">**HDN\_ITEMCHANGEDW** (Unicode) and **HDN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



 

 






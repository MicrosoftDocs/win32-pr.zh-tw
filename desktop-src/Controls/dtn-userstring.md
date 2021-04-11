---
title: 'DTN_USERSTRING (Commctrl 的通知碼) '
description: 當使用者完成編輯控制項中的字串時，日期和時間選擇器會傳送 (DTP) 控制項。
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- DTN_USERSTRING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843208"
---
# <a name="dtn_userstring-notification-code"></a><span data-ttu-id="1bf80-104">DTN \_ USERSTRING 通知碼</span><span class="sxs-lookup"><span data-stu-id="1bf80-104">DTN\_USERSTRING notification code</span></span>

<span data-ttu-id="1bf80-105">當使用者完成編輯控制項中的字串時，日期和時間選擇器會傳送 (DTP) 控制項。</span><span class="sxs-lookup"><span data-stu-id="1bf80-105">Sent by a date and time picker (DTP) control when a user finishes editing a string in the control.</span></span> <span data-ttu-id="1bf80-106">只有設定為 [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) 樣式的 DTP 控制項才會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="1bf80-106">This notification code is only sent by DTP controls that are set to the [**DTS\_APPCANPARSE**](date-and-time-picker-control-styles.md) style.</span></span> <span data-ttu-id="1bf80-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="1bf80-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1bf80-108">參數</span><span class="sxs-lookup"><span data-stu-id="1bf80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bf80-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1bf80-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bf80-110">[**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa)結構的指標，其中包含通知碼實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1bf80-110">A pointer to an [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) structure that contains information about the instance of the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bf80-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1bf80-111">Return value</span></span>

<span data-ttu-id="1bf80-112">控制項的擁有者必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="1bf80-112">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bf80-113">備註</span><span class="sxs-lookup"><span data-stu-id="1bf80-113">Remarks</span></span>

<span data-ttu-id="1bf80-114">處理此通知碼可讓擁有者將自訂回應提供給使用者在控制項中輸入的字串。</span><span class="sxs-lookup"><span data-stu-id="1bf80-114">Handling this notification code allows the owner to provide custom responses to strings entered into the control by the user.</span></span> <span data-ttu-id="1bf80-115">擁有者必須準備好剖析輸入字串，並視需要採取動作。</span><span class="sxs-lookup"><span data-stu-id="1bf80-115">The owner must be prepared to parse the input string and take action if necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf80-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bf80-116">Requirements</span></span>



| <span data-ttu-id="1bf80-117">需求</span><span class="sxs-lookup"><span data-stu-id="1bf80-117">Requirement</span></span> | <span data-ttu-id="1bf80-118">值</span><span class="sxs-lookup"><span data-stu-id="1bf80-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf80-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1bf80-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf80-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bf80-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1bf80-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1bf80-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf80-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bf80-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1bf80-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1bf80-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bf80-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1bf80-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1bf80-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1bf80-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1bf80-126">**DTN \_USERSTRINGW** (Unicode) 和 **DTN \_ USERSTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="1bf80-126">**DTN\_USERSTRINGW** (Unicode) and **DTN\_USERSTRINGA** (ANSI)</span></span><br/>             |



 

 






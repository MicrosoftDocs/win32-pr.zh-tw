---
title: 'PSN_GETOBJECT (Prsht.idl 的通知碼) '
description: 由屬性工作表傳送，以在游標通過其中一個索引標籤控制項按鈕時，要求放置目標物件。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024800"
---
# <a name="psn_getobject-notification-code"></a><span data-ttu-id="a3460-105">PSN \_ GETOBJECT 通知碼</span><span class="sxs-lookup"><span data-stu-id="a3460-105">PSN\_GETOBJECT notification code</span></span>

<span data-ttu-id="a3460-106">由屬性工作表傳送，以在游標通過其中一個索引標籤控制項按鈕時，要求放置目標物件。</span><span class="sxs-lookup"><span data-stu-id="a3460-106">Sent by a property sheet to request a drop target object when the cursor passes over one of the tab control's buttons.</span></span> <span data-ttu-id="a3460-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="a3460-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a3460-108">參數</span><span class="sxs-lookup"><span data-stu-id="a3460-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3460-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3460-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3460-110">[**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的指標，該結構會在進入時包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a3460-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that, on entry, contains information about the notification code.</span></span> <span data-ttu-id="a3460-111">如果已處理此通知程式碼，您必須將物件資訊插入此結構中。</span><span class="sxs-lookup"><span data-stu-id="a3460-111">If this notification code is processed, you must insert object information into this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3460-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3460-112">Return value</span></span>

<span data-ttu-id="a3460-113">處理此通知程式碼的應用程式必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="a3460-113">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3460-114">備註</span><span class="sxs-lookup"><span data-stu-id="a3460-114">Remarks</span></span>

<span data-ttu-id="a3460-115">若要提供物件，應用程式必須在 *lParam* 的部分 [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的成員中設定值。</span><span class="sxs-lookup"><span data-stu-id="a3460-115">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="a3460-116">**PObject** 成員必須設定為有效的物件指標，且 **hResult** 成員必須設定為成功旗標。</span><span class="sxs-lookup"><span data-stu-id="a3460-116">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="a3460-117">為了符合元件物件模型 (COM) 標準，請在提供物件指標時，一律遞增物件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="a3460-117">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="a3460-118">如果應用程式不提供物件，則必須將 **pObject** 設定為 **Null** ，並將 **hResult** 設定為失敗旗標。</span><span class="sxs-lookup"><span data-stu-id="a3460-118">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

> [!Note]  
> <span data-ttu-id="a3460-119">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此通知碼。</span><span class="sxs-lookup"><span data-stu-id="a3460-119">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a3460-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3460-120">Requirements</span></span>



| <span data-ttu-id="a3460-121">需求</span><span class="sxs-lookup"><span data-stu-id="a3460-121">Requirement</span></span> | <span data-ttu-id="a3460-122">值</span><span class="sxs-lookup"><span data-stu-id="a3460-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3460-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3460-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a3460-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3460-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a3460-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3460-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a3460-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3460-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a3460-127">標頭</span><span class="sxs-lookup"><span data-stu-id="a3460-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3460-128"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a3460-128"><dt>Prsht.h</dt></span></span> </dl> |



 

 






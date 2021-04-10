---
title: 'TBN_GETOBJECT (Commctrl 的通知碼) '
description: 由使用 TBSTYLE REGISTERDROP 樣式的工具列控制項所傳送， \_ 以在指標通過其按鈕時，要求放置目標物件。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- TBN_GETOBJECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093808"
---
# <a name="tbn_getobject-notification-code"></a><span data-ttu-id="964a0-105">TBN \_ GETOBJECT 通知碼</span><span class="sxs-lookup"><span data-stu-id="964a0-105">TBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="964a0-106">由使用 [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) 樣式的工具列控制項所傳送，以在指標通過其按鈕時，要求放置目標物件。</span><span class="sxs-lookup"><span data-stu-id="964a0-106">Sent by a toolbar control that uses the [**TBSTYLE\_REGISTERDROP**](toolbar-control-and-button-styles.md) style to request a drop target object when the pointer passes over one of its buttons.</span></span> <span data-ttu-id="964a0-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="964a0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="964a0-108">參數</span><span class="sxs-lookup"><span data-stu-id="964a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="964a0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="964a0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="964a0-110">[**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的指標，其中包含指標所傳遞之按鈕的相關資訊，並接收應用程式提供的資料，以回應此通知碼。</span><span class="sxs-lookup"><span data-stu-id="964a0-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the button that the pointer passed over and receives data the application provides in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="964a0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="964a0-111">Return value</span></span>

<span data-ttu-id="964a0-112">處理此通知程式碼的應用程式必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="964a0-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="964a0-113">備註</span><span class="sxs-lookup"><span data-stu-id="964a0-113">Remarks</span></span>

<span data-ttu-id="964a0-114">若要提供物件，應用程式必須在 *lParam* 的部分 [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的成員中設定值。</span><span class="sxs-lookup"><span data-stu-id="964a0-114">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="964a0-115">**PObject** 成員必須設定為有效的物件指標，且 **hResult** 成員必須設定為成功旗標。</span><span class="sxs-lookup"><span data-stu-id="964a0-115">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="964a0-116">為了符合元件物件模型 (COM) 標準，請在提供物件指標時，一律遞增物件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="964a0-116">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="964a0-117">如果應用程式不提供物件，則必須將 **pObject** 設定為 **Null** ，並將 **hResult** 設定為失敗旗標。</span><span class="sxs-lookup"><span data-stu-id="964a0-117">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="964a0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="964a0-118">Requirements</span></span>



| <span data-ttu-id="964a0-119">需求</span><span class="sxs-lookup"><span data-stu-id="964a0-119">Requirement</span></span> | <span data-ttu-id="964a0-120">值</span><span class="sxs-lookup"><span data-stu-id="964a0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="964a0-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="964a0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="964a0-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="964a0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="964a0-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="964a0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="964a0-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="964a0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="964a0-125">標頭</span><span class="sxs-lookup"><span data-stu-id="964a0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="964a0-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="964a0-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






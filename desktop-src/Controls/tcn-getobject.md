---
title: 'TCN_GETOBJECT (Commctrl 的通知碼) '
description: 當索引標籤控制項具有 TCS \_ EX \_ REGISTERDROP 擴充樣式，且將物件拖曳至控制項中的索引標籤專案上方時，便會傳送此控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965691"
---
# <a name="tcn_getobject-notification-code"></a><span data-ttu-id="15f14-105">TCN \_ GETOBJECT 通知碼</span><span class="sxs-lookup"><span data-stu-id="15f14-105">TCN\_GETOBJECT notification code</span></span>

<span data-ttu-id="15f14-106">當索引標籤控制項具有 [**TCS \_ EX \_ REGISTERDROP**](tab-control-extended-styles.md) 擴充樣式，且將物件拖曳至控制項中的索引標籤專案上方時，便會傳送此控制項。</span><span class="sxs-lookup"><span data-stu-id="15f14-106">Sent by a tab control when it has the [**TCS\_EX\_REGISTERDROP**](tab-control-extended-styles.md) extended style and an object is dragged over a tab item in the control.</span></span> <span data-ttu-id="15f14-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="15f14-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="15f14-108">參數</span><span class="sxs-lookup"><span data-stu-id="15f14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15f14-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15f14-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15f14-110">[**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的指標，其中包含物件拖曳到的索引標籤專案的相關資訊，並接收應用程式傳回的資料以回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="15f14-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the tab item the object is dragged over and receives data the application returns in response to this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15f14-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="15f14-111">Return value</span></span>

<span data-ttu-id="15f14-112">處理此通知程式碼的應用程式必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="15f14-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="15f14-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="15f14-113">Requirements</span></span>



| <span data-ttu-id="15f14-114">需求</span><span class="sxs-lookup"><span data-stu-id="15f14-114">Requirement</span></span> | <span data-ttu-id="15f14-115">值</span><span class="sxs-lookup"><span data-stu-id="15f14-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15f14-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15f14-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15f14-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15f14-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="15f14-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15f14-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15f14-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15f14-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="15f14-120">標頭</span><span class="sxs-lookup"><span data-stu-id="15f14-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="15f14-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="15f14-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






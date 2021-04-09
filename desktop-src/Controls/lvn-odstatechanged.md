---
title: 'LVN_ODSTATECHANGED (Commctrl 的通知碼) '
description: 當專案或專案範圍的狀態變更時，由清單視圖控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: a3aafda5-a3ec-4f84-8153-8d34097e04f1
keywords:
- LVN_ODSTATECHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ODSTATECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86de2f5e01e15d0a97c49f451914aac5b74b27e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686170"
---
# <a name="lvn_odstatechanged-notification-code"></a><span data-ttu-id="de2b9-105">LVN \_ ODSTATECHANGED 通知碼</span><span class="sxs-lookup"><span data-stu-id="de2b9-105">LVN\_ODSTATECHANGED notification code</span></span>

<span data-ttu-id="de2b9-106">當專案或專案範圍的狀態變更時，由清單視圖控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="de2b9-106">Sent by a list-view control when the state of an item or range of items has changed.</span></span> <span data-ttu-id="de2b9-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="de2b9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODSTATECHANGED

    lpStateChange = (LPNMLVODSTATECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="de2b9-108">參數</span><span class="sxs-lookup"><span data-stu-id="de2b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de2b9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de2b9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de2b9-110">[**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange)結構的指標，其中包含已變更之專案或專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="de2b9-110">Pointer to an [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) structure that contains information about the item or items that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de2b9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="de2b9-111">Return value</span></span>

<span data-ttu-id="de2b9-112">接收此通知碼的應用程式必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="de2b9-112">The application receiving this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="de2b9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="de2b9-113">Requirements</span></span>



| <span data-ttu-id="de2b9-114">需求</span><span class="sxs-lookup"><span data-stu-id="de2b9-114">Requirement</span></span> | <span data-ttu-id="de2b9-115">值</span><span class="sxs-lookup"><span data-stu-id="de2b9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de2b9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de2b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de2b9-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de2b9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de2b9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de2b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de2b9-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de2b9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de2b9-120">標頭</span><span class="sxs-lookup"><span data-stu-id="de2b9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="de2b9-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="de2b9-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






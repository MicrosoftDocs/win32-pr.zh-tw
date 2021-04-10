---
title: 'BCN_HOTITEMCHANGE (Commctrl 的通知碼) '
description: 通知按鈕控制項擁有者滑鼠正在進入或離開按鈕控制項的工作區。 按鈕控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- BCN_HOTITEMCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024936"
---
# <a name="bcn_hotitemchange-notification-code"></a><span data-ttu-id="7759d-105">BCN \_ HOTITEMCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="7759d-105">BCN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="7759d-106">通知按鈕控制項擁有者滑鼠正在進入或離開按鈕控制項的工作區。</span><span class="sxs-lookup"><span data-stu-id="7759d-106">Notifies the button control owner that the mouse is entering or leaving the client area of the button control.</span></span> <span data-ttu-id="7759d-107">按鈕控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="7759d-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7759d-108">參數</span><span class="sxs-lookup"><span data-stu-id="7759d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7759d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7759d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7759d-110">[**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7759d-110">A pointer to a [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7759d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7759d-111">Return value</span></span>

<span data-ttu-id="7759d-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7759d-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7759d-113">備註</span><span class="sxs-lookup"><span data-stu-id="7759d-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7759d-114">若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="7759d-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="7759d-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="7759d-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7759d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7759d-116">Requirements</span></span>



| <span data-ttu-id="7759d-117">需求</span><span class="sxs-lookup"><span data-stu-id="7759d-117">Requirement</span></span> | <span data-ttu-id="7759d-118">值</span><span class="sxs-lookup"><span data-stu-id="7759d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7759d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7759d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7759d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7759d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7759d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7759d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7759d-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7759d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7759d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7759d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7759d-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7759d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






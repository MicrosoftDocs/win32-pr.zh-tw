---
title: 'RBN_DELETEDBAND (Commctrl 的通知碼) '
description: 在刪除帶狀之後，由 Rebar 控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ef4aca07-de08-47de-b236-321e84e6e81c
keywords:
- RBN_DELETEDBAND 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_DELETEDBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af4e107ccb1a42b82335255f48d0328e03019a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843916"
---
# <a name="rbn_deletedband-notification-code"></a><span data-ttu-id="0ebf0-105">RBN \_ DELETEDBAND 通知碼</span><span class="sxs-lookup"><span data-stu-id="0ebf0-105">RBN\_DELETEDBAND notification code</span></span>

<span data-ttu-id="0ebf0-106">在刪除帶狀之後，由 Rebar 控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="0ebf0-106">Sent by a rebar control after a band has been deleted.</span></span> <span data-ttu-id="0ebf0-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="0ebf0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETEDBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0ebf0-108">參數</span><span class="sxs-lookup"><span data-stu-id="0ebf0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ebf0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ebf0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebf0-110">[**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ebf0-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ebf0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ebf0-111">Return value</span></span>

<span data-ttu-id="0ebf0-112">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="0ebf0-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebf0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ebf0-113">Requirements</span></span>



| <span data-ttu-id="0ebf0-114">需求</span><span class="sxs-lookup"><span data-stu-id="0ebf0-114">Requirement</span></span> | <span data-ttu-id="0ebf0-115">值</span><span class="sxs-lookup"><span data-stu-id="0ebf0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebf0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ebf0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0ebf0-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ebf0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ebf0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ebf0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0ebf0-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ebf0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ebf0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0ebf0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ebf0-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ebf0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: 'RBN_CHILDSIZE (Commctrl 的通知碼) '
description: 當調整寬線的子視窗大小時，由 Rebar 控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ba64d21a-e568-4894-8007-be644ae4f54a
keywords:
- RBN_CHILDSIZE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_CHILDSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d505d13048d96783d53b9b1a821d80712597da4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843788"
---
# <a name="rbn_childsize-notification-code"></a><span data-ttu-id="90afe-105">RBN \_ CHILDSIZE 通知碼</span><span class="sxs-lookup"><span data-stu-id="90afe-105">RBN\_CHILDSIZE notification code</span></span>

<span data-ttu-id="90afe-106">當調整寬線的子視窗大小時，由 Rebar 控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="90afe-106">Sent by a rebar control when a band's child window is resized.</span></span> <span data-ttu-id="90afe-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="90afe-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHILDSIZE

    lprbcs = (LPNMREBARCHILDSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="90afe-108">參數</span><span class="sxs-lookup"><span data-stu-id="90afe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90afe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90afe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90afe-110">[**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="90afe-110">Pointer to an [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90afe-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="90afe-111">Return value</span></span>

<span data-ttu-id="90afe-112">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="90afe-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="90afe-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="90afe-113">Requirements</span></span>



| <span data-ttu-id="90afe-114">需求</span><span class="sxs-lookup"><span data-stu-id="90afe-114">Requirement</span></span> | <span data-ttu-id="90afe-115">值</span><span class="sxs-lookup"><span data-stu-id="90afe-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90afe-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90afe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="90afe-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90afe-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90afe-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90afe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="90afe-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90afe-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90afe-120">標頭</span><span class="sxs-lookup"><span data-stu-id="90afe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="90afe-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="90afe-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: 'RBN_MINMAX (Commctrl 的通知碼) '
description: 在最大化或最小化寬線之前，由 Rebar 控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- RBN_MINMAX 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106984958"
---
# <a name="rbn_minmax-notification-code"></a><span data-ttu-id="2a370-105">RBN \_ MINMAX 通知碼</span><span class="sxs-lookup"><span data-stu-id="2a370-105">RBN\_MINMAX notification code</span></span>

<span data-ttu-id="2a370-106">在最大化或最小化寬線之前，由 Rebar 控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="2a370-106">Sent by a rebar control prior to maximizing or minimizing a band.</span></span> <span data-ttu-id="2a370-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="2a370-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_MINMAX
```



## <a name="parameters"></a><span data-ttu-id="2a370-108">參數</span><span class="sxs-lookup"><span data-stu-id="2a370-108">Parameters</span></span>

<span data-ttu-id="2a370-109">此通知碼沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2a370-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a370-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a370-110">Return value</span></span>

<span data-ttu-id="2a370-111">傳回非零值以防止作業發生，零允許它繼續。</span><span class="sxs-lookup"><span data-stu-id="2a370-111">Return a nonzero value to prevent the operation from taking place, zero to allow it to continue.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a370-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a370-112">Requirements</span></span>



| <span data-ttu-id="2a370-113">需求</span><span class="sxs-lookup"><span data-stu-id="2a370-113">Requirement</span></span> | <span data-ttu-id="2a370-114">值</span><span class="sxs-lookup"><span data-stu-id="2a370-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a370-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a370-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2a370-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a370-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a370-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a370-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2a370-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a370-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a370-119">標頭</span><span class="sxs-lookup"><span data-stu-id="2a370-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a370-120"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a370-120"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






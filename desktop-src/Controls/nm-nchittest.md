---
title: 'NM_NCHITTEST (Commctrl 的通知碼) '
description: NM_NCHITTEST 通知碼-當控制項收到 WM NCHITTEST 訊息時，由 Rebar 控制項傳送 \_ 。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ede0ac017fbe5146cd68e51e2a38c7f66c7898
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112316"
---
# <a name="nm_nchittest-notification-code"></a><span data-ttu-id="5602c-105">NM \_ NCHITTEST 通知碼</span><span class="sxs-lookup"><span data-stu-id="5602c-105">NM\_NCHITTEST notification code</span></span>

<span data-ttu-id="5602c-106">當控制項收到 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) 訊息時，由 Rebar 控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="5602c-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="5602c-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="5602c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5602c-108">參數</span><span class="sxs-lookup"><span data-stu-id="5602c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5602c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5602c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5602c-110">[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5602c-110">A pointer to a [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="5602c-111">*Pt* 成員包含點擊測試訊息的滑鼠座標。</span><span class="sxs-lookup"><span data-stu-id="5602c-111">The *pt* member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5602c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5602c-112">Return value</span></span>

<span data-ttu-id="5602c-113">除非另有指定，否則會傳回零以允許控制項執行點擊測試訊息的預設處理，或傳回 \* 在 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) 下記載的其中一個 HT 值以覆寫預設的點擊測試處理。</span><span class="sxs-lookup"><span data-stu-id="5602c-113">Unless otherwise specified, return zero to allow the control to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5602c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5602c-114">Requirements</span></span>



| <span data-ttu-id="5602c-115">需求</span><span class="sxs-lookup"><span data-stu-id="5602c-115">Requirement</span></span> | <span data-ttu-id="5602c-116">值</span><span class="sxs-lookup"><span data-stu-id="5602c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5602c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5602c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5602c-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5602c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5602c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5602c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5602c-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5602c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5602c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5602c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5602c-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5602c-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


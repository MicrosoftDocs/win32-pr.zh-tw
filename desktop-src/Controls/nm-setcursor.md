---
title: 'NM_SETCURSOR (Commctrl 的通知碼) '
description: 通知控制項的父視窗，控制項正在設定資料指標以回應 WM \_ SETCURSOR 訊息。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 8d70563f-05a3-4116-b686-6d9063940fae
keywords:
- NM_SETCURSOR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cc3c48a0224efec0c8ab8844a3e7f234a9ba51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094299"
---
# <a name="nm_setcursor-notification-code"></a><span data-ttu-id="8c1d3-105">NM \_ SETCURSOR 通知碼</span><span class="sxs-lookup"><span data-stu-id="8c1d3-105">NM\_SETCURSOR notification code</span></span>

<span data-ttu-id="8c1d3-106">通知控制項的父視窗，控制項正在設定資料指標以回應 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息。</span><span class="sxs-lookup"><span data-stu-id="8c1d3-106">Notifies a control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="8c1d3-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="8c1d3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8c1d3-108">參數</span><span class="sxs-lookup"><span data-stu-id="8c1d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c1d3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c1d3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c1d3-110">[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8c1d3-110">A pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c1d3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c1d3-111">Return value</span></span>

<span data-ttu-id="8c1d3-112">傳回零以讓控制項設定資料指標或非零值，以防止控制項設定資料指標。</span><span class="sxs-lookup"><span data-stu-id="8c1d3-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c1d3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c1d3-113">Requirements</span></span>



| <span data-ttu-id="8c1d3-114">需求</span><span class="sxs-lookup"><span data-stu-id="8c1d3-114">Requirement</span></span> | <span data-ttu-id="8c1d3-115">值</span><span class="sxs-lookup"><span data-stu-id="8c1d3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c1d3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c1d3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8c1d3-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c1d3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c1d3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c1d3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8c1d3-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c1d3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c1d3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="8c1d3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c1d3-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c1d3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 


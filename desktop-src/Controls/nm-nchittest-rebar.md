---
title: 'NM_NCHITTEST (Rebar) 通知碼 (Commctrl) '
description: 當控制項收到 WM NCHITTEST 訊息時，由 Rebar 控制項傳送 \_ 。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- NM_NCHITTEST (Rebar) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 4fb4568cad87017d9fff94deb60583ac0b4c1d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105096"
---
# <a name="nm_nchittest-rebar-notification-code"></a><span data-ttu-id="d76d1-105">NM \_ NCHITTEST (Rebar) 通知碼</span><span class="sxs-lookup"><span data-stu-id="d76d1-105">NM\_NCHITTEST (rebar) notification code</span></span>

<span data-ttu-id="d76d1-106">當控制項收到 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) 訊息時，由 Rebar 控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="d76d1-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="d76d1-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d76d1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d76d1-108">參數</span><span class="sxs-lookup"><span data-stu-id="d76d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d76d1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d76d1-110">[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d76d1-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="d76d1-111">**DwItemSpec** 成員包含發生點擊測試訊息的頻外索引，而 **pt** 成員則包含點擊測試訊息的滑鼠座標。</span><span class="sxs-lookup"><span data-stu-id="d76d1-111">The **dwItemSpec** member contains the band index over which the hit test message occurred, and the **pt** member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d76d1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d76d1-112">Return value</span></span>

<span data-ttu-id="d76d1-113">傳回零以允許 Rebar 執行點擊測試訊息的預設處理，或傳回 \* 在 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) 下記載的其中一個 HT 值以覆寫預設點擊測試處理。</span><span class="sxs-lookup"><span data-stu-id="d76d1-113">Return zero to allow the rebar to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d76d1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d76d1-114">Requirements</span></span>



| <span data-ttu-id="d76d1-115">需求</span><span class="sxs-lookup"><span data-stu-id="d76d1-115">Requirement</span></span> | <span data-ttu-id="d76d1-116">值</span><span class="sxs-lookup"><span data-stu-id="d76d1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d76d1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d76d1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d76d1-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d76d1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d76d1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d76d1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d76d1-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d76d1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d76d1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d76d1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d76d1-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d76d1-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


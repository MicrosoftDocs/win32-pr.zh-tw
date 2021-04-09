---
title: 'NM_SETCURSOR (ComboBoxEx) 通知碼 (Commctrl .h) '
description: 通知 ComboBoxEx 控制項的父視窗，控制項正在設定資料指標以回應 WM \_ SETCURSOR 訊息。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- NM_SETCURSOR (ComboBoxEx) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 5fbd5e10f06e74af0778521d31c69e63586a6476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686199"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a><span data-ttu-id="965ea-105">NM \_ SETCURSOR (ComboBoxEx) 通知碼</span><span class="sxs-lookup"><span data-stu-id="965ea-105">NM\_SETCURSOR (ComboBoxEx) notification code</span></span>

<span data-ttu-id="965ea-106">通知 ComboBoxEx 控制項的父視窗，控制項正在設定資料指標以回應 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息。</span><span class="sxs-lookup"><span data-stu-id="965ea-106">Notifies a ComboBoxEx control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="965ea-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="965ea-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="965ea-108">參數</span><span class="sxs-lookup"><span data-stu-id="965ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="965ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="965ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="965ea-110">[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="965ea-110">A pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="965ea-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="965ea-111">Return value</span></span>

<span data-ttu-id="965ea-112">傳回零以讓控制項設定資料指標或非零值，以防止控制項設定資料指標。</span><span class="sxs-lookup"><span data-stu-id="965ea-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="965ea-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="965ea-113">Requirements</span></span>



| <span data-ttu-id="965ea-114">需求</span><span class="sxs-lookup"><span data-stu-id="965ea-114">Requirement</span></span> | <span data-ttu-id="965ea-115">值</span><span class="sxs-lookup"><span data-stu-id="965ea-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="965ea-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="965ea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="965ea-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="965ea-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="965ea-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="965ea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="965ea-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="965ea-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="965ea-120">標頭</span><span class="sxs-lookup"><span data-stu-id="965ea-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="965ea-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="965ea-121"><dt>Commctrl.h</dt></span></span> </dl> |



 


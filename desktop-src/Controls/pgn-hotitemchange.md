---
title: 'PGN_HOTITEMCHANGE 訊息 (Commctrl .h) '
description: 通知頁面控制項的父視窗，其中的熱 (反白顯示) 專案已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- PGN_HOTITEMCHANGE message Windows 控制項
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 573f3dd93a6e4b0b3db6682d36804416d6f6f1e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024989"
---
# <a name="pgn_hotitemchange-message"></a><span data-ttu-id="e5b3b-105">PGN \_ HOTITEMCHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="e5b3b-105">PGN\_HOTITEMCHANGE message</span></span>

<span data-ttu-id="e5b3b-106">通知頁面控制項的父視窗，其中的熱 (反白顯示) 專案已變更。</span><span class="sxs-lookup"><span data-stu-id="e5b3b-106">Notifies a pager control's parent window that the hot (highlighted) item has change.</span></span> <span data-ttu-id="e5b3b-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="e5b3b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e5b3b-108">參數</span><span class="sxs-lookup"><span data-stu-id="e5b3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b3b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5b3b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5b3b-110">[**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5b3b-110">Pointer to a [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5b3b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5b3b-111">Return value</span></span>

<span data-ttu-id="e5b3b-112">傳回零，以反白顯示專案或非零，以防止反白顯示。</span><span class="sxs-lookup"><span data-stu-id="e5b3b-112">Return zero to highlight the item or nonzero to prevent highlighting.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5b3b-113">備註</span><span class="sxs-lookup"><span data-stu-id="e5b3b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e5b3b-114">若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="e5b3b-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e5b3b-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="e5b3b-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5b3b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5b3b-116">Requirements</span></span>



| <span data-ttu-id="e5b3b-117">需求</span><span class="sxs-lookup"><span data-stu-id="e5b3b-117">Requirement</span></span> | <span data-ttu-id="e5b3b-118">值</span><span class="sxs-lookup"><span data-stu-id="e5b3b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b3b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5b3b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b3b-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5b3b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e5b3b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5b3b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b3b-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5b3b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5b3b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e5b3b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5b3b-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e5b3b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






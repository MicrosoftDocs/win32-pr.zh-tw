---
title: 'TBN_HOTITEMCHANGE (Commctrl 的通知碼) '
description: 當熱 (反白顯示) 專案變更時，由工具列控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- TBN_HOTITEMCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685505"
---
# <a name="tbn_hotitemchange-notification-code"></a><span data-ttu-id="cf3cc-105">TBN \_ HOTITEMCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="cf3cc-105">TBN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="cf3cc-106">當熱 (反白顯示) 專案變更時，由工具列控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="cf3cc-106">Sent by a toolbar control when the hot (highlighted) item changes.</span></span> <span data-ttu-id="cf3cc-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="cf3cc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cf3cc-108">參數</span><span class="sxs-lookup"><span data-stu-id="cf3cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf3cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf3cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf3cc-110">[**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cf3cc-110">Pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf3cc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf3cc-111">Return value</span></span>

<span data-ttu-id="cf3cc-112">傳回零以允許反白顯示專案，或傳回非零值以防止專案反白顯示。</span><span class="sxs-lookup"><span data-stu-id="cf3cc-112">Return zero to allow the item to be highlighted, or nonzero to prevent the item from being highlighted.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf3cc-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf3cc-113">Requirements</span></span>



| <span data-ttu-id="cf3cc-114">需求</span><span class="sxs-lookup"><span data-stu-id="cf3cc-114">Requirement</span></span> | <span data-ttu-id="cf3cc-115">值</span><span class="sxs-lookup"><span data-stu-id="cf3cc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf3cc-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf3cc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cf3cc-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf3cc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf3cc-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf3cc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cf3cc-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf3cc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf3cc-120">標頭</span><span class="sxs-lookup"><span data-stu-id="cf3cc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf3cc-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf3cc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






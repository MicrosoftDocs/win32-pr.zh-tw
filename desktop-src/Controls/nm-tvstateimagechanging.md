---
title: 'NM_TVSTATEIMAGECHANGING (Commctrl 的通知碼) '
description: 由樹狀檢視控制項傳送至其父視窗，表示狀態影像正在變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 8e42d8b3-5e76-4d03-94b0-3e4583669095
keywords:
- NM_TVSTATEIMAGECHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_TVSTATEIMAGECHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf628eb9387acd4fd10f100f2f80570d1b021b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094292"
---
# <a name="nm_tvstateimagechanging-notification-code"></a><span data-ttu-id="08e9a-105">NM \_ TVSTATEIMAGECHANGING 通知碼</span><span class="sxs-lookup"><span data-stu-id="08e9a-105">NM\_TVSTATEIMAGECHANGING notification code</span></span>

<span data-ttu-id="08e9a-106">由樹狀檢視控制項傳送至其父視窗，表示狀態影像正在變更。</span><span class="sxs-lookup"><span data-stu-id="08e9a-106">Sent by a tree-view control to its parent window that the state image is changing.</span></span> <span data-ttu-id="08e9a-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="08e9a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TVSTATEIMAGECHANGING
        
    lpnmtsic = (LPNMTVSTATEIMAGECHANGING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="08e9a-108">參數</span><span class="sxs-lookup"><span data-stu-id="08e9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08e9a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08e9a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08e9a-110">[**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="08e9a-110">A pointer to an [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08e9a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="08e9a-111">Return value</span></span>

<span data-ttu-id="08e9a-112">控制項會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="08e9a-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="08e9a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="08e9a-113">Requirements</span></span>



| <span data-ttu-id="08e9a-114">需求</span><span class="sxs-lookup"><span data-stu-id="08e9a-114">Requirement</span></span> | <span data-ttu-id="08e9a-115">值</span><span class="sxs-lookup"><span data-stu-id="08e9a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08e9a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08e9a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="08e9a-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08e9a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08e9a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08e9a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="08e9a-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08e9a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08e9a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="08e9a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="08e9a-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="08e9a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






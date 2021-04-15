---
title: 'EN_PARAGRAPHEXPANDED (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父系已展開大綱。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: D33EB118-FC79-4284-820B-3424F13722C4
keywords:
- EN_PARAGRAPHEXPANDED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_PARAGRAPHEXPANDEDC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f862260c0653d23b0b53649a2c05e59820e3808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465484"
---
# <a name="en_paragraphexpanded-notification-code"></a><span data-ttu-id="375e8-105">EN \_ PARAGRAPHEXPANDED 通知碼</span><span class="sxs-lookup"><span data-stu-id="375e8-105">EN\_PARAGRAPHEXPANDED notification code</span></span>

<span data-ttu-id="375e8-106">通知 rich edit 控制項的父系已展開大綱。</span><span class="sxs-lookup"><span data-stu-id="375e8-106">Notifies a rich edit control's parent that an outline has been expanded.</span></span> <span data-ttu-id="375e8-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="375e8-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PARAGRAPHEXPANDED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="375e8-108">參數</span><span class="sxs-lookup"><span data-stu-id="375e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="375e8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="375e8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="375e8-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構。</span><span class="sxs-lookup"><span data-stu-id="375e8-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="375e8-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="375e8-111">Requirements</span></span>



| <span data-ttu-id="375e8-112">需求</span><span class="sxs-lookup"><span data-stu-id="375e8-112">Requirement</span></span> | <span data-ttu-id="375e8-113">值</span><span class="sxs-lookup"><span data-stu-id="375e8-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="375e8-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="375e8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="375e8-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="375e8-115">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="375e8-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="375e8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="375e8-117">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="375e8-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="375e8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="375e8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="375e8-119"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="375e8-119"><dt>Richedit.h</dt></span></span> </dl> |



 

 






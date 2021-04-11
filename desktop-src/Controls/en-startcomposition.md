---
title: 'EN_STARTCOMPOSITION (Richedit 的通知碼) '
description: 通知 rich edit 控制項父視窗，使用者已開始輸入 IME 或文字服務架構。
ms.assetid: 755C0C5F-061B-44AF-98A5-776AEE1B7AF8
keywords:
- EN_STARTCOMPOSITION 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_STARTCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a103431427a9325a6b74c27927fb56e65f6fe771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105557"
---
# <a name="en_startcomposition-notification-code"></a><span data-ttu-id="7ceeb-104">EN \_ STARTCOMPOSITION 通知碼</span><span class="sxs-lookup"><span data-stu-id="7ceeb-104">EN\_STARTCOMPOSITION notification code</span></span>

<span data-ttu-id="7ceeb-105">通知 rich edit 控制項父視窗，使用者已開始輸入 IME 或 [文字服務架構](/windows/desktop/TSF/text-services-framework)。</span><span class="sxs-lookup"><span data-stu-id="7ceeb-105">Notifies a rich edit control parent window that the user started typing with IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_STARTCOMPOSITION

    pStartComp = (NMDHR *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7ceeb-106">參數</span><span class="sxs-lookup"><span data-stu-id="7ceeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ceeb-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ceeb-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ceeb-108">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構。</span><span class="sxs-lookup"><span data-stu-id="7ceeb-108">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ceeb-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ceeb-109">Requirements</span></span>



| <span data-ttu-id="7ceeb-110">需求</span><span class="sxs-lookup"><span data-stu-id="7ceeb-110">Requirement</span></span> | <span data-ttu-id="7ceeb-111">值</span><span class="sxs-lookup"><span data-stu-id="7ceeb-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ceeb-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ceeb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="7ceeb-113">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ceeb-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7ceeb-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ceeb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="7ceeb-115">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ceeb-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ceeb-116">標頭</span><span class="sxs-lookup"><span data-stu-id="7ceeb-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ceeb-117"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ceeb-117"><dt>Richedit.h</dt></span></span> </dl> |



 


---
title: 'NM_FONTCHANGED (Commctrl 的通知碼) '
description: 當控制項變更字型時，由清單視圖控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ffa019b0-34be-4bb3-b9dd-c267545fec84
keywords:
- NM_FONTCHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_FONTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75003021f83276c953b5aa2cf0b812d20d60857b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843079"
---
# <a name="nm_fontchanged-notification-code"></a><span data-ttu-id="a8c4e-105">NM \_ FONTCHANGED 通知碼</span><span class="sxs-lookup"><span data-stu-id="a8c4e-105">NM\_FONTCHANGED notification code</span></span>

<span data-ttu-id="a8c4e-106">當控制項變更字型時，由清單視圖控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="a8c4e-106">Sent by a list-view control when the control has changed a font.</span></span> <span data-ttu-id="a8c4e-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="a8c4e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_FONTCHANGED
        
    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a8c4e-108">參數</span><span class="sxs-lookup"><span data-stu-id="a8c4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8c4e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8c4e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8c4e-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a8c4e-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8c4e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8c4e-111">Return value</span></span>

<span data-ttu-id="a8c4e-112">控制項會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="a8c4e-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c4e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8c4e-113">Requirements</span></span>



| <span data-ttu-id="a8c4e-114">需求</span><span class="sxs-lookup"><span data-stu-id="a8c4e-114">Requirement</span></span> | <span data-ttu-id="a8c4e-115">值</span><span class="sxs-lookup"><span data-stu-id="a8c4e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c4e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8c4e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a8c4e-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8c4e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8c4e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8c4e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a8c4e-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8c4e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8c4e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a8c4e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8c4e-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8c4e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: 'NM_OUTOFMEMORY (Commctrl 的通知碼) '
description: 通知控制項的父視窗，控制項無法完成作業，因為沒有足夠的可用記憶體。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- NM_OUTOFMEMORY 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1321f88360d168b13d16b36f984d9b797dc094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024656"
---
# <a name="nm_outofmemory-notification-code"></a><span data-ttu-id="040ff-105">NM \_ OUTOFMEMORY 通知碼</span><span class="sxs-lookup"><span data-stu-id="040ff-105">NM\_OUTOFMEMORY notification code</span></span>

<span data-ttu-id="040ff-106">通知控制項的父視窗，控制項無法完成作業，因為沒有足夠的可用記憶體。</span><span class="sxs-lookup"><span data-stu-id="040ff-106">Notifies a control's parent window that the control could not complete an operation because there was not enough memory available.</span></span> <span data-ttu-id="040ff-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="040ff-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="040ff-108">參數</span><span class="sxs-lookup"><span data-stu-id="040ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="040ff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="040ff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="040ff-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="040ff-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="040ff-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="040ff-111">Return value</span></span>

<span data-ttu-id="040ff-112">控制項會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="040ff-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="040ff-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="040ff-113">Requirements</span></span>



| <span data-ttu-id="040ff-114">需求</span><span class="sxs-lookup"><span data-stu-id="040ff-114">Requirement</span></span> | <span data-ttu-id="040ff-115">值</span><span class="sxs-lookup"><span data-stu-id="040ff-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="040ff-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="040ff-116">Minimum supported client</span></span><br/> | <span data-ttu-id="040ff-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="040ff-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="040ff-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="040ff-118">Minimum supported server</span></span><br/> | <span data-ttu-id="040ff-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="040ff-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="040ff-120">標頭</span><span class="sxs-lookup"><span data-stu-id="040ff-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="040ff-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="040ff-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






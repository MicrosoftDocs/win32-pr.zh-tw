---
title: 'TBN_ENDDRAG (Commctrl 的通知碼) '
description: 通知工具列的父視窗，指出使用者已停止拖曳工具列中的按鈕。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 846ba42e-6e0d-45bb-88ce-7b4d2cb17e13
keywords:
- TBN_ENDDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd493ac338e11716ea381e83102b200334a1eec4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105030"
---
# <a name="tbn_enddrag-notification-code"></a><span data-ttu-id="73786-105">TBN \_ ENDDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="73786-105">TBN\_ENDDRAG notification code</span></span>

<span data-ttu-id="73786-106">通知工具列的父視窗，指出使用者已停止拖曳工具列中的按鈕。</span><span class="sxs-lookup"><span data-stu-id="73786-106">Notifies the toolbar's parent window that the user has stopped dragging a button in a toolbar.</span></span> <span data-ttu-id="73786-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="73786-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="73786-108">參數</span><span class="sxs-lookup"><span data-stu-id="73786-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73786-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73786-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73786-110">[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="73786-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="73786-111">**IItem** 成員包含所拖曳按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="73786-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73786-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="73786-112">Return value</span></span>

<span data-ttu-id="73786-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="73786-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="73786-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="73786-114">Requirements</span></span>



| <span data-ttu-id="73786-115">需求</span><span class="sxs-lookup"><span data-stu-id="73786-115">Requirement</span></span> | <span data-ttu-id="73786-116">值</span><span class="sxs-lookup"><span data-stu-id="73786-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73786-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73786-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73786-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73786-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73786-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73786-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73786-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73786-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73786-121">標頭</span><span class="sxs-lookup"><span data-stu-id="73786-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="73786-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="73786-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






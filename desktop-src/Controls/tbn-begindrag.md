---
title: 'TBN_BEGINDRAG (Commctrl 的通知碼) '
description: 通知工具列的父視窗，指出使用者已開始拖曳工具列中的按鈕。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 244406e5-e13d-4c80-81fa-81b018b29ec1
keywords:
- TBN_BEGINDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cfa7325d1a8e1eab27383d7df918c8896933bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094167"
---
# <a name="tbn_begindrag-notification-code"></a><span data-ttu-id="25e94-105">TBN \_ BEGINDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="25e94-105">TBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="25e94-106">通知工具列的父視窗，指出使用者已開始拖曳工具列中的按鈕。</span><span class="sxs-lookup"><span data-stu-id="25e94-106">Notifies a toolbar's parent window that the user has begun dragging a button in a toolbar.</span></span> <span data-ttu-id="25e94-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="25e94-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_BEGINDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="25e94-108">參數</span><span class="sxs-lookup"><span data-stu-id="25e94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25e94-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25e94-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25e94-110">[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="25e94-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="25e94-111">**IItem** 成員包含所拖曳按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="25e94-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25e94-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="25e94-112">Return value</span></span>

<span data-ttu-id="25e94-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="25e94-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="25e94-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="25e94-114">Requirements</span></span>



| <span data-ttu-id="25e94-115">需求</span><span class="sxs-lookup"><span data-stu-id="25e94-115">Requirement</span></span> | <span data-ttu-id="25e94-116">值</span><span class="sxs-lookup"><span data-stu-id="25e94-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25e94-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25e94-117">Minimum supported client</span></span><br/> | <span data-ttu-id="25e94-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25e94-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25e94-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25e94-119">Minimum supported server</span></span><br/> | <span data-ttu-id="25e94-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25e94-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25e94-121">標頭</span><span class="sxs-lookup"><span data-stu-id="25e94-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="25e94-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="25e94-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






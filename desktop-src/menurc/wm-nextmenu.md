---
title: 'WM_NEXTMENU 訊息 (Winuser .h) '
description: 當使用向右鍵或向左鍵切換至功能表列和系統功能表時，傳送至應用程式。
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935126"
---
# <a name="wm_nextmenu-message"></a><span data-ttu-id="30a89-104">WM \_ NEXTMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="30a89-104">WM\_NEXTMENU message</span></span>

<span data-ttu-id="30a89-105">當使用向右鍵或向左鍵切換至功能表列和系統功能表時，傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="30a89-105">Sent to an application when the right or left arrow key is used to switch between the menu bar and the system menu.</span></span>


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a><span data-ttu-id="30a89-106">參數</span><span class="sxs-lookup"><span data-stu-id="30a89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a89-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30a89-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30a89-108">金鑰的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="30a89-108">The virtual-key code of the key.</span></span> <span data-ttu-id="30a89-109">請參閱 [**虛擬金鑰代碼**](/windows/desktop/inputdev/virtual-key-codes)。</span><span class="sxs-lookup"><span data-stu-id="30a89-109">See [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="30a89-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30a89-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30a89-111">[**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)結構的指標，其中包含要啟用之功能表的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="30a89-111">A pointer to a [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) structure that contains information about the menu to be activated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30a89-112">備註</span><span class="sxs-lookup"><span data-stu-id="30a89-112">Remarks</span></span>

<span data-ttu-id="30a89-113">回應此訊息時，應用程式可以在 [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)的 **hmenuNext** 成員中指定要切換的功能表，並在視窗中指定要在 **MDINEXTMENU** 結構的 **hwndNext** 成員中接收功能表通知訊息的功能表。</span><span class="sxs-lookup"><span data-stu-id="30a89-113">In responding to this message, the application can specify the menu to switch to in the **hmenuNext** member of [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) and the window to receive the menu notification messages in the **hwndNext** member of the **MDINEXTMENU** structure.</span></span> <span data-ttu-id="30a89-114">您必須設定這兩個成員，變更才會生效 (這些成員最初是 **Null**) 。</span><span class="sxs-lookup"><span data-stu-id="30a89-114">You must set both members for the changes to take effect (they are initially **NULL**).</span></span>

## <a name="requirements"></a><span data-ttu-id="30a89-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="30a89-115">Requirements</span></span>



| <span data-ttu-id="30a89-116">需求</span><span class="sxs-lookup"><span data-stu-id="30a89-116">Requirement</span></span> | <span data-ttu-id="30a89-117">值</span><span class="sxs-lookup"><span data-stu-id="30a89-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a89-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30a89-118">Minimum supported client</span></span><br/> | <span data-ttu-id="30a89-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30a89-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="30a89-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30a89-120">Minimum supported server</span></span><br/> | <span data-ttu-id="30a89-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30a89-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30a89-122">標頭</span><span class="sxs-lookup"><span data-stu-id="30a89-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="30a89-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="30a89-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a89-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30a89-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="30a89-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="30a89-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="30a89-126">**MDINEXTMENU**</span><span class="sxs-lookup"><span data-stu-id="30a89-126">**MDINEXTMENU**</span></span>](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

<span data-ttu-id="30a89-127">**概念**</span><span class="sxs-lookup"><span data-stu-id="30a89-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="30a89-128">功能表</span><span class="sxs-lookup"><span data-stu-id="30a89-128">Menus</span></span>](menus.md)
</dt> </dl>

 


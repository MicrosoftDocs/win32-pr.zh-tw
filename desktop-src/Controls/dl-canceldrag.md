---
title: 'DL_CANCELDRAG (Commctrl 的通知碼) '
description: 藉由按一下滑鼠右鍵或按下 ESC 鍵，表示使用者已取消拖曳作業。
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- DL_CANCELDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106691"
---
# <a name="dl_canceldrag-notification-code"></a><span data-ttu-id="2a147-104">DL \_ CANCELDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="2a147-104">DL\_CANCELDRAG notification code</span></span>

<span data-ttu-id="2a147-105">藉由按一下滑鼠右鍵或按下 ESC 鍵，表示使用者已取消拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="2a147-105">Signals that the user has canceled a drag operation by clicking the right mouse button or pressing the ESC key.</span></span> <span data-ttu-id="2a147-106">拖曳清單方塊會將此通知碼以拖曳清單訊息的形式傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="2a147-106">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="2a147-107">如需詳細資訊，請參閱 [拖曳清單方塊訊息](about-list-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="2a147-107">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2a147-108">參數</span><span class="sxs-lookup"><span data-stu-id="2a147-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a147-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a147-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a147-110">[**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)結構的指標，其中包含 DL \_ CANCELDRAG 通知碼、拖曳清單方塊的控制碼，以及游標位置。</span><span class="sxs-lookup"><span data-stu-id="2a147-110">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_CANCELDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a147-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a147-111">Return value</span></span>

<span data-ttu-id="2a147-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="2a147-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a147-113">備註</span><span class="sxs-lookup"><span data-stu-id="2a147-113">Remarks</span></span>

<span data-ttu-id="2a147-114">藉由處理 DL \_ CANCELDRAG 通知程式碼，應用程式可以重設其內部狀態，以指出拖曳沒有作用。</span><span class="sxs-lookup"><span data-stu-id="2a147-114">By processing the DL\_CANCELDRAG notification code, an application can reset its internal state to indicate that dragging is not in effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a147-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a147-115">Requirements</span></span>



| <span data-ttu-id="2a147-116">需求</span><span class="sxs-lookup"><span data-stu-id="2a147-116">Requirement</span></span> | <span data-ttu-id="2a147-117">值</span><span class="sxs-lookup"><span data-stu-id="2a147-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a147-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a147-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2a147-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a147-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a147-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a147-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2a147-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a147-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a147-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2a147-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a147-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a147-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






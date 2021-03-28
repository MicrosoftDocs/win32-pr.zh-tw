---
description: 指示使用新的 DROPDESCRIPTION 資訊來更新放置映射視窗。
title: DDWM_UPDATEWINDOW 訊息
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bff0e007c735fcf202aaf16cf304eb4ff5358f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972028"
---
# <a name="ddwm_updatewindow-message"></a><span data-ttu-id="5cb89-103">DDWM \_ UPDATEWINDOW 訊息</span><span class="sxs-lookup"><span data-stu-id="5cb89-103">DDWM\_UPDATEWINDOW message</span></span>

<span data-ttu-id="5cb89-104">指示使用新的 [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) 資訊來更新放置映射視窗。</span><span class="sxs-lookup"><span data-stu-id="5cb89-104">Instructs a drop image window to update using new [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) information.</span></span>

## <a name="parameters"></a><span data-ttu-id="5cb89-105">參數</span><span class="sxs-lookup"><span data-stu-id="5cb89-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cb89-106">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5cb89-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cb89-107">未使用。</span><span class="sxs-lookup"><span data-stu-id="5cb89-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5cb89-108">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5cb89-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cb89-109">未使用。</span><span class="sxs-lookup"><span data-stu-id="5cb89-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cb89-110">備註</span><span class="sxs-lookup"><span data-stu-id="5cb89-110">Remarks</span></span>

<span data-ttu-id="5cb89-111">DDWM \_ UPDATEWINDOW 定義為 WM \_ 使用者 + 3。</span><span class="sxs-lookup"><span data-stu-id="5cb89-111">DDWM\_UPDATEWINDOW is defined as WM\_USER+3.</span></span>

<span data-ttu-id="5cb89-112">當 drop 作業的狀態變更時（例如回應輔助按鍵），[**IDropTarget：:D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) 會傳回新的 [**DROPEFFECT**](../com/dropeffect-constants.md) 值 (這個 **DROPEFFECT** 值也可以透過 [**IDropSource：： system.windows.dragdrop.givefeedback>**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)) 來接收。</span><span class="sxs-lookup"><span data-stu-id="5cb89-112">When the state of a drop operation changes—such as in response to a modifier key—[**IDropTarget::DragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) returns a new [**DROPEFFECT**](../com/dropeffect-constants.md) value (this **DROPEFFECT** value can also be received through [**IDropSource::GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span></span> <span data-ttu-id="5cb89-113">在回應中，應用程式會使用新的 [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype)值來更新放置目標的 [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription)結構，以指出要套用至拖曳視窗視覺效果的裝飾;例如，指出檔案正在複製而不是移動，或物件無法卸載至該位置。</span><span class="sxs-lookup"><span data-stu-id="5cb89-113">In response, the application updates the drop target's [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) structure with a new [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) value that indicates the decoration to be applied to the drag window's visual; for instance, an indication that the file is being copied rather than moved or that the object cannot be dropped to that location.</span></span> <span data-ttu-id="5cb89-114">不過，在物件收到 **DDWM \_ UPDATEWINDOW** 訊息之前，不會更新視覺效果。</span><span class="sxs-lookup"><span data-stu-id="5cb89-114">However, the visuals are not updated until the object receives a **DDWM\_UPDATEWINDOW** message.</span></span>

<span data-ttu-id="5cb89-115">[DragWindow](clipboard.md)剪貼簿格式會將「收件者」視窗的 **HWND** ，提供給 **DDWM \_ UPDATEWINDOW** 訊息的寄件者。</span><span class="sxs-lookup"><span data-stu-id="5cb89-115">The [DragWindow](clipboard.md) clipboard format provides the **HWND** of the recipient drag window to the sender of the **DDWM\_UPDATEWINDOW** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cb89-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cb89-116">Requirements</span></span>



| <span data-ttu-id="5cb89-117">需求</span><span class="sxs-lookup"><span data-stu-id="5cb89-117">Requirement</span></span> | <span data-ttu-id="5cb89-118">值</span><span class="sxs-lookup"><span data-stu-id="5cb89-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5cb89-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5cb89-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5cb89-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cb89-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5cb89-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5cb89-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5cb89-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cb89-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 

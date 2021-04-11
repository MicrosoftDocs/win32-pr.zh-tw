---
title: 'TB_GETOBJECT 訊息 (Commctrl .h) '
description: 抓取工具列控制項的 IDropTarget。
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- TB_GETOBJECT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105054"
---
# <a name="tb_getobject-message"></a><span data-ttu-id="fe784-104">TB \_ GETOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="fe784-104">TB\_GETOBJECT message</span></span>

<span data-ttu-id="fe784-105">抓取工具列控制項的 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) 。</span><span class="sxs-lookup"><span data-stu-id="fe784-105">Retrieves the [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe784-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe784-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe784-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe784-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe784-108">所要求之介面的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe784-108">Identifier of the interface being requested.</span></span> <span data-ttu-id="fe784-109">此值必須指向 **IID \_ IDropTarget**。</span><span class="sxs-lookup"><span data-stu-id="fe784-109">This value must point to **IID\_IDropTarget**.</span></span>

</dd> <dt>

<span data-ttu-id="fe784-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe784-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe784-111">接收介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="fe784-111">Address that receives the interface pointer.</span></span> <span data-ttu-id="fe784-112">如果發生錯誤，則會在此位址中放置 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="fe784-112">If an error occurs, a **NULL** pointer is placed in this address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe784-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe784-113">Return value</span></span>

<span data-ttu-id="fe784-114">傳回 **HRESULT** 值，指出作業成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="fe784-114">Returns an **HRESULT** value indicating success or failure of the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe784-115">備註</span><span class="sxs-lookup"><span data-stu-id="fe784-115">Remarks</span></span>

<span data-ttu-id="fe784-116">工具列的 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) 會在將物件拖曳至其上方或卸載時，供工具列使用。</span><span class="sxs-lookup"><span data-stu-id="fe784-116">The toolbar's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) is used by the toolbar when objects are dragged over or dropped onto it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe784-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe784-117">Requirements</span></span>



| <span data-ttu-id="fe784-118">需求</span><span class="sxs-lookup"><span data-stu-id="fe784-118">Requirement</span></span> | <span data-ttu-id="fe784-119">值</span><span class="sxs-lookup"><span data-stu-id="fe784-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe784-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe784-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe784-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe784-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe784-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe784-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe784-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe784-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe784-124">標頭</span><span class="sxs-lookup"><span data-stu-id="fe784-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe784-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe784-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


---
description: 管理延遲的應用程式暫停作業。
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: 'ISuspendingDeferral 介面 (Windows. ApplicationModel) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972857"
---
# <a name="isuspendingdeferral-interface"></a><span data-ttu-id="8de7c-103">ISuspendingDeferral 介面</span><span class="sxs-lookup"><span data-stu-id="8de7c-103">ISuspendingDeferral interface</span></span>

<span data-ttu-id="8de7c-104">管理延遲的應用程式暫停作業。</span><span class="sxs-lookup"><span data-stu-id="8de7c-104">Manages a delayed app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="8de7c-105">成員</span><span class="sxs-lookup"><span data-stu-id="8de7c-105">Members</span></span>

<span data-ttu-id="8de7c-106">**ISuspendingDeferral** 介面繼承自 [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)。</span><span class="sxs-lookup"><span data-stu-id="8de7c-106">The **ISuspendingDeferral** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="8de7c-107">**ISuspendingDeferral** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8de7c-107">**ISuspendingDeferral** also has these types of members:</span></span>

-   [<span data-ttu-id="8de7c-108">方法</span><span class="sxs-lookup"><span data-stu-id="8de7c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8de7c-109">方法</span><span class="sxs-lookup"><span data-stu-id="8de7c-109">Methods</span></span>

<span data-ttu-id="8de7c-110">**ISuspendingDeferral** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8de7c-110">The **ISuspendingDeferral** interface has these methods.</span></span>



| <span data-ttu-id="8de7c-111">方法</span><span class="sxs-lookup"><span data-stu-id="8de7c-111">Method</span></span>                                           | <span data-ttu-id="8de7c-112">描述</span><span class="sxs-lookup"><span data-stu-id="8de7c-112">Description</span></span>                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8de7c-113">**完成**</span><span class="sxs-lookup"><span data-stu-id="8de7c-113">**Complete**</span></span>](isuspendingdeferral-complete.md) | <span data-ttu-id="8de7c-114">通知系統應用程式已儲存其資料，並已準備好暫停。</span><span class="sxs-lookup"><span data-stu-id="8de7c-114">Notifies the system that the app has saved its data and is ready to be suspended.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8de7c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8de7c-115">Requirements</span></span>



| <span data-ttu-id="8de7c-116">需求</span><span class="sxs-lookup"><span data-stu-id="8de7c-116">Requirement</span></span> | <span data-ttu-id="8de7c-117">值</span><span class="sxs-lookup"><span data-stu-id="8de7c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8de7c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8de7c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8de7c-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8de7c-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8de7c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8de7c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8de7c-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8de7c-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8de7c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8de7c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8de7c-123"><dt>ApplicationModel。h</dt></span><span class="sxs-lookup"><span data-stu-id="8de7c-123"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="8de7c-124">Idl</span><span class="sxs-lookup"><span data-stu-id="8de7c-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8de7c-125"><dt>ApplicationModel .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8de7c-125"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8de7c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8de7c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de7c-127">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="8de7c-127">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="8de7c-128">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="8de7c-128">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> <dt>

[<span data-ttu-id="8de7c-129">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="8de7c-129">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 

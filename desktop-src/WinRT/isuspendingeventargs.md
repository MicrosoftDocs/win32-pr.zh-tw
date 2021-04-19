---
description: 提供應用程式暫停事件的資料。
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: 'ISuspendingEventArgs 介面 (Windows. ApplicationModel) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970175"
---
# <a name="isuspendingeventargs-interface"></a><span data-ttu-id="8893c-103">ISuspendingEventArgs 介面</span><span class="sxs-lookup"><span data-stu-id="8893c-103">ISuspendingEventArgs interface</span></span>

<span data-ttu-id="8893c-104">提供應用程式暫停事件的資料。</span><span class="sxs-lookup"><span data-stu-id="8893c-104">Provides data for an app suspending event.</span></span>

## <a name="members"></a><span data-ttu-id="8893c-105">成員</span><span class="sxs-lookup"><span data-stu-id="8893c-105">Members</span></span>

<span data-ttu-id="8893c-106">**ISuspendingEventArgs** 介面繼承自 [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)。</span><span class="sxs-lookup"><span data-stu-id="8893c-106">The **ISuspendingEventArgs** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="8893c-107">**ISuspendingEventArgs** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8893c-107">**ISuspendingEventArgs** also has these types of members:</span></span>

-   [<span data-ttu-id="8893c-108">屬性</span><span class="sxs-lookup"><span data-stu-id="8893c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8893c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8893c-109">Properties</span></span>

<span data-ttu-id="8893c-110">**ISuspendingEventArgs** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8893c-110">The **ISuspendingEventArgs** interface has these properties.</span></span>



| <span data-ttu-id="8893c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8893c-111">Property</span></span>                                                                           | <span data-ttu-id="8893c-112">存取類型</span><span class="sxs-lookup"><span data-stu-id="8893c-112">Access type</span></span>           | <span data-ttu-id="8893c-113">Description</span><span class="sxs-lookup"><span data-stu-id="8893c-113">Description</span></span>                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="8893c-114">**SuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="8893c-114">**SuspendingOperation**</span></span>](isuspendingeventargs-suspendingoperation.md)<br/> | <span data-ttu-id="8893c-115">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8893c-115">Read/write</span></span><br/> | <span data-ttu-id="8893c-116">取得應用程式暫停作業。</span><span class="sxs-lookup"><span data-stu-id="8893c-116">Gets the app suspending operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8893c-117">備註</span><span class="sxs-lookup"><span data-stu-id="8893c-117">Remarks</span></span>

<span data-ttu-id="8893c-118">當您執行事件處理常式（例如 [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041)、 [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)），並 [**新增 \_ 暫停**](/previous-versions//hh438376(v=vs.85)) 以回應應用程式暫止事件時，就會存取這個物件。</span><span class="sxs-lookup"><span data-stu-id="8893c-118">This object is accessed when you implement event handlers like [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041), and [**add\_Suspending**](/previous-versions//hh438376(v=vs.85)) to respond to app suspending events.</span></span>

## <a name="requirements"></a><span data-ttu-id="8893c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8893c-119">Requirements</span></span>



| <span data-ttu-id="8893c-120">需求</span><span class="sxs-lookup"><span data-stu-id="8893c-120">Requirement</span></span> | <span data-ttu-id="8893c-121">值</span><span class="sxs-lookup"><span data-stu-id="8893c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8893c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8893c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8893c-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8893c-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8893c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8893c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8893c-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8893c-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8893c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="8893c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8893c-127"><dt>ApplicationModel。h</dt></span><span class="sxs-lookup"><span data-stu-id="8893c-127"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="8893c-128">Idl</span><span class="sxs-lookup"><span data-stu-id="8893c-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8893c-129"><dt>ApplicationModel .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8893c-129"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8893c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8893c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8893c-131">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="8893c-131">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="8893c-132">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="8893c-132">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> <dt>

[<span data-ttu-id="8893c-133">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="8893c-133">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 

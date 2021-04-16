---
description: 提供應用程式暫停作業的相關資訊。
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: 'ISuspendingOperation 介面 (Windows. ApplicationModel) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511476"
---
# <a name="isuspendingoperation-interface"></a><span data-ttu-id="5dcc3-103">ISuspendingOperation 介面</span><span class="sxs-lookup"><span data-stu-id="5dcc3-103">ISuspendingOperation interface</span></span>

<span data-ttu-id="5dcc3-104">提供應用程式暫停作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5dcc3-104">Provides information about an app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="5dcc3-105">成員</span><span class="sxs-lookup"><span data-stu-id="5dcc3-105">Members</span></span>

<span data-ttu-id="5dcc3-106">**ISuspendingOperation** 介面繼承自 [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)。</span><span class="sxs-lookup"><span data-stu-id="5dcc3-106">The **ISuspendingOperation** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="5dcc3-107">**ISuspendingOperation** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5dcc3-107">**ISuspendingOperation** also has these types of members:</span></span>

-   [<span data-ttu-id="5dcc3-108">方法</span><span class="sxs-lookup"><span data-stu-id="5dcc3-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="5dcc3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="5dcc3-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5dcc3-110">方法</span><span class="sxs-lookup"><span data-stu-id="5dcc3-110">Methods</span></span>

<span data-ttu-id="5dcc3-111">**ISuspendingOperation** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5dcc3-111">The **ISuspendingOperation** interface has these methods.</span></span>



| <span data-ttu-id="5dcc3-112">方法</span><span class="sxs-lookup"><span data-stu-id="5dcc3-112">Method</span></span>                                                  | <span data-ttu-id="5dcc3-113">描述</span><span class="sxs-lookup"><span data-stu-id="5dcc3-113">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="5dcc3-114">**GetDeferral**</span><span class="sxs-lookup"><span data-stu-id="5dcc3-114">**GetDeferral**</span></span>](isuspendingoperation-getdeferral.md) | <span data-ttu-id="5dcc3-115">要求應用程式暫停操作延遲。</span><span class="sxs-lookup"><span data-stu-id="5dcc3-115">Requests that the app suspending operation be delayed.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5dcc3-116">屬性</span><span class="sxs-lookup"><span data-stu-id="5dcc3-116">Properties</span></span>

<span data-ttu-id="5dcc3-117">**ISuspendingOperation** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5dcc3-117">The **ISuspendingOperation** interface has these properties.</span></span>



| <span data-ttu-id="5dcc3-118">屬性</span><span class="sxs-lookup"><span data-stu-id="5dcc3-118">Property</span></span>                                                     | <span data-ttu-id="5dcc3-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="5dcc3-119">Access type</span></span>           | <span data-ttu-id="5dcc3-120">Description</span><span class="sxs-lookup"><span data-stu-id="5dcc3-120">Description</span></span>                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dcc3-121">**期限**</span><span class="sxs-lookup"><span data-stu-id="5dcc3-121">**Deadline**</span></span>](isuspendingoperation-deadline.md)<br/> | <span data-ttu-id="5dcc3-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5dcc3-122">Read/write</span></span><br/> | <span data-ttu-id="5dcc3-123">取得延遲的應用程式暫停作業繼續之前剩餘的時間。</span><span class="sxs-lookup"><span data-stu-id="5dcc3-123">Gets the time remaining before a delayed app suspending operation continues.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5dcc3-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5dcc3-124">Requirements</span></span>



| <span data-ttu-id="5dcc3-125">需求</span><span class="sxs-lookup"><span data-stu-id="5dcc3-125">Requirement</span></span> | <span data-ttu-id="5dcc3-126">值</span><span class="sxs-lookup"><span data-stu-id="5dcc3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dcc3-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5dcc3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5dcc3-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5dcc3-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5dcc3-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5dcc3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5dcc3-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5dcc3-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5dcc3-131">標頭</span><span class="sxs-lookup"><span data-stu-id="5dcc3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dcc3-132"><dt>ApplicationModel。h</dt></span><span class="sxs-lookup"><span data-stu-id="5dcc3-132"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="5dcc3-133">Idl</span><span class="sxs-lookup"><span data-stu-id="5dcc3-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5dcc3-134"><dt>ApplicationModel .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5dcc3-134"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dcc3-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5dcc3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dcc3-136">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="5dcc3-136">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="5dcc3-137">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="5dcc3-137">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> <dt>

[<span data-ttu-id="5dcc3-138">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="5dcc3-138">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 

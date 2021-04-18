---
description: 提供 VectorChanged 事件的資料。
ms.assetid: 635c0f96-5d64-436e-9186-78f9d85b6d29
title: 'IVectorChangedEventArgs 介面 (IVectorChangedEventArgs .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: d5e1405c87d0c2a0c41a0244f79cea7b2e86ea40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511473"
---
# <a name="ivectorchangedeventargs-interface"></a><span data-ttu-id="8dc17-103">IVectorChangedEventArgs 介面</span><span class="sxs-lookup"><span data-stu-id="8dc17-103">IVectorChangedEventArgs interface</span></span>

<span data-ttu-id="8dc17-104">提供 [**VectorChanged**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) 事件的資料。</span><span class="sxs-lookup"><span data-stu-id="8dc17-104">Provides data for a [**VectorChanged**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) event.</span></span>

## <a name="members"></a><span data-ttu-id="8dc17-105">成員</span><span class="sxs-lookup"><span data-stu-id="8dc17-105">Members</span></span>

<span data-ttu-id="8dc17-106">**IVectorChangedEventArgs** 介面繼承自 **IInspectable**。</span><span class="sxs-lookup"><span data-stu-id="8dc17-106">The **IVectorChangedEventArgs** interface inherits from **IInspectable**.</span></span> <span data-ttu-id="8dc17-107">**IVectorChangedEventArgs** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8dc17-107">**IVectorChangedEventArgs** also has these types of members:</span></span>

-   [<span data-ttu-id="8dc17-108">方法</span><span class="sxs-lookup"><span data-stu-id="8dc17-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8dc17-109">方法</span><span class="sxs-lookup"><span data-stu-id="8dc17-109">Methods</span></span>

<span data-ttu-id="8dc17-110">**IVectorChangedEventArgs** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8dc17-110">The **IVectorChangedEventArgs** interface has these methods.</span></span>



| <span data-ttu-id="8dc17-111">方法</span><span class="sxs-lookup"><span data-stu-id="8dc17-111">Method</span></span>                                                                        | <span data-ttu-id="8dc17-112">描述</span><span class="sxs-lookup"><span data-stu-id="8dc17-112">Description</span></span>                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="8dc17-113">**取得 \_ CollectionChange**</span><span class="sxs-lookup"><span data-stu-id="8dc17-113">**get\_CollectionChange**</span></span>](ivectorchangedeventargs-get-collectionchange.md) | <span data-ttu-id="8dc17-114">取得在向量中發生的變更類型。</span><span class="sxs-lookup"><span data-stu-id="8dc17-114">Gets the type of change that occurred in the vector.</span></span><br/>       |
| [<span data-ttu-id="8dc17-115">**取得 \_ 索引**</span><span class="sxs-lookup"><span data-stu-id="8dc17-115">**get\_Index**</span></span>](ivectorchangedeventargs-get-index.md)                       | <span data-ttu-id="8dc17-116">取得向量中發生變更的位置。</span><span class="sxs-lookup"><span data-stu-id="8dc17-116">Gets the position in the vector where the change occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8dc17-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8dc17-117">Requirements</span></span>



| <span data-ttu-id="8dc17-118">需求</span><span class="sxs-lookup"><span data-stu-id="8dc17-118">Requirement</span></span> | <span data-ttu-id="8dc17-119">值</span><span class="sxs-lookup"><span data-stu-id="8dc17-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc17-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8dc17-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8dc17-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8dc17-121">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="8dc17-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8dc17-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8dc17-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8dc17-123">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="8dc17-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8dc17-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dc17-125"><dt>IVectorChangedEventArgs。h</dt></span><span class="sxs-lookup"><span data-stu-id="8dc17-125"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



 

 

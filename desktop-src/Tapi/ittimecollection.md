---
description: ITTimeCollection 介面是會話描述項通訊協定 (SDP) 會議 blob 物件的提供者特定介面。
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: 'ITTimeCollection 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992570"
---
# <a name="ittimecollection-interface"></a><span data-ttu-id="ad21a-103">ITTimeCollection 介面</span><span class="sxs-lookup"><span data-stu-id="ad21a-103">ITTimeCollection interface</span></span>

<span data-ttu-id="ad21a-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="ad21a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ad21a-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ad21a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ad21a-106">**ITTimeCollection** 介面是會話描述項通訊協定 (SDP) 會議 blob 物件的提供者特定介面。</span><span class="sxs-lookup"><span data-stu-id="ad21a-106">The **ITTimeCollection** interface is a provider-specific interface for the Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="ad21a-107">此介面可讓您依索引存取 [**ITTime**](ittime.md) 介面，也可讓您建立和刪除時間元件。</span><span class="sxs-lookup"><span data-stu-id="ad21a-107">This interface allows access to [**ITTime**](ittime.md) interfaces by index, and also enable the creation and deletion of time components.</span></span> <span data-ttu-id="ad21a-108">[**ITSdp：： get \_ TimeCollection**](itsdp-get-timecollection.md)方法會建立 **ITTimeCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="ad21a-108">The [**ITSdp::get\_TimeCollection**](itsdp-get-timecollection.md) method creates the **ITTimeCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="ad21a-109">成員</span><span class="sxs-lookup"><span data-stu-id="ad21a-109">Members</span></span>

<span data-ttu-id="ad21a-110">**ITTimeCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="ad21a-110">The **ITTimeCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ad21a-111">**ITTimeCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ad21a-111">**ITTimeCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="ad21a-112">方法</span><span class="sxs-lookup"><span data-stu-id="ad21a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ad21a-113">方法</span><span class="sxs-lookup"><span data-stu-id="ad21a-113">Methods</span></span>

<span data-ttu-id="ad21a-114">**ITTimeCollection** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ad21a-114">The **ITTimeCollection** interface has these methods.</span></span>



| <span data-ttu-id="ad21a-115">方法</span><span class="sxs-lookup"><span data-stu-id="ad21a-115">Method</span></span>                                                           | <span data-ttu-id="ad21a-116">描述</span><span class="sxs-lookup"><span data-stu-id="ad21a-116">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad21a-117">**創建**</span><span class="sxs-lookup"><span data-stu-id="ad21a-117">**Create**</span></span>](ittimecollection-create.md)                        | <span data-ttu-id="ad21a-118">建立 [**ITTime**](ittime.md) 元件。</span><span class="sxs-lookup"><span data-stu-id="ad21a-118">Creates an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="ad21a-119">**刪除**</span><span class="sxs-lookup"><span data-stu-id="ad21a-119">**Delete**</span></span>](ittimecollection-delete.md)                        | <span data-ttu-id="ad21a-120">刪除 [**ITTime**](ittime.md) 元件。</span><span class="sxs-lookup"><span data-stu-id="ad21a-120">Deletes an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="ad21a-121">**取得 \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="ad21a-121">**get\_\_NewEnum**</span></span>](ittimecollection-get--newenum.md)          | <span data-ttu-id="ad21a-122">傳回集合的列舉程式。</span><span class="sxs-lookup"><span data-stu-id="ad21a-122">Returns an enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="ad21a-123">**取得 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="ad21a-123">**get\_Count**</span></span>](ittimecollection-get-count.md)                 | <span data-ttu-id="ad21a-124">取得集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="ad21a-124">Gets number of items in collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="ad21a-125">**取得 \_ EnumerationIf**</span><span class="sxs-lookup"><span data-stu-id="ad21a-125">**get\_EnumerationIf**</span></span>](ittimecollection-get-enumerationif.md) | <span data-ttu-id="ad21a-126">傳回列舉 [**ITTime**](ittime.md)的 [**IEnumTime**](ienumtime.md)列舉介面。</span><span class="sxs-lookup"><span data-stu-id="ad21a-126">Returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span><br/> |
| [<span data-ttu-id="ad21a-127">**取得 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="ad21a-127">**get\_Item**</span></span>](ittimecollection-get-item.md)                   | <span data-ttu-id="ad21a-128">指定索引之後，會傳回集合中的專案。</span><span class="sxs-lookup"><span data-stu-id="ad21a-128">Given an index, returns an item in the collection.</span></span><br/>                                                         |



 

## <a name="requirements"></a><span data-ttu-id="ad21a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad21a-129">Requirements</span></span>



| <span data-ttu-id="ad21a-130">需求</span><span class="sxs-lookup"><span data-stu-id="ad21a-130">Requirement</span></span> | <span data-ttu-id="ad21a-131">值</span><span class="sxs-lookup"><span data-stu-id="ad21a-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad21a-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ad21a-132">TAPI version</span></span><br/> | <span data-ttu-id="ad21a-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ad21a-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ad21a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="ad21a-134">Header</span></span><br/>       | <dl> <span data-ttu-id="ad21a-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad21a-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad21a-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="ad21a-136">Library</span></span><br/>      | <dl> <span data-ttu-id="ad21a-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="ad21a-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ad21a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ad21a-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="ad21a-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad21a-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 


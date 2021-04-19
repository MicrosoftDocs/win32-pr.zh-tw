---
description: ITMediaCollection 介面可讓您存取 SDP (RFC 2327) 會議描述中的一組媒體資訊。
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: 'ITMediaCollection 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21305e1d1729437b53c380b7712feee3827b3ba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997441"
---
# <a name="itmediacollection-interface"></a><span data-ttu-id="9afc8-103">ITMediaCollection 介面</span><span class="sxs-lookup"><span data-stu-id="9afc8-103">ITMediaCollection interface</span></span>

<span data-ttu-id="9afc8-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="9afc8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9afc8-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="9afc8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9afc8-106">**ITMediaCollection** 介面可讓您存取 SDP (RFC 2327) 會議描述中的一組媒體資訊。</span><span class="sxs-lookup"><span data-stu-id="9afc8-106">The **ITMediaCollection** interface provides access to the set of media information in an SDP (RFC 2327) conference description.</span></span> <span data-ttu-id="9afc8-107">[**ITMedia**](itmedia.md)介面會描述 SDP 中的每個媒體描述。</span><span class="sxs-lookup"><span data-stu-id="9afc8-107">Each Media description in the SDP is described by an [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="9afc8-108">**ITMediaCollection** 可讓您操作一組 SDP 的 **ITMedia** 資訊，包括：</span><span class="sxs-lookup"><span data-stu-id="9afc8-108">**ITMediaCollection** allows manipulation of the set of **ITMedia** information for the SDP, including:</span></span>

-   <span data-ttu-id="9afc8-109">允許依索引存取媒體。</span><span class="sxs-lookup"><span data-stu-id="9afc8-109">Allows media access by index.</span></span>
-   <span data-ttu-id="9afc8-110">啟用媒體的建立和刪除。</span><span class="sxs-lookup"><span data-stu-id="9afc8-110">Enables creation and deletion of media.</span></span>

<span data-ttu-id="9afc8-111">[**ITSdp：： get \_ MediaCollection**](itsdp-get-mediacollection.md)方法會建立 **ITMediaCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="9afc8-111">The [**ITSdp::get\_MediaCollection**](itsdp-get-mediacollection.md) method creates the **ITMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="9afc8-112">成員</span><span class="sxs-lookup"><span data-stu-id="9afc8-112">Members</span></span>

<span data-ttu-id="9afc8-113">**ITMediaCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="9afc8-113">The **ITMediaCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9afc8-114">**ITMediaCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9afc8-114">**ITMediaCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="9afc8-115">方法</span><span class="sxs-lookup"><span data-stu-id="9afc8-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9afc8-116">方法</span><span class="sxs-lookup"><span data-stu-id="9afc8-116">Methods</span></span>

<span data-ttu-id="9afc8-117">**ITMediaCollection** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9afc8-117">The **ITMediaCollection** interface has these methods.</span></span>



| <span data-ttu-id="9afc8-118">方法</span><span class="sxs-lookup"><span data-stu-id="9afc8-118">Method</span></span>                                                            | <span data-ttu-id="9afc8-119">描述</span><span class="sxs-lookup"><span data-stu-id="9afc8-119">Description</span></span>                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="9afc8-120">**創建**</span><span class="sxs-lookup"><span data-stu-id="9afc8-120">**Create**</span></span>](itmediacollection-create.md)                        | <span data-ttu-id="9afc8-121">使用預設屬性建立新的媒體，並將其傳回。</span><span class="sxs-lookup"><span data-stu-id="9afc8-121">Creates a new media with default properties and returns it.</span></span><br/> |
| [<span data-ttu-id="9afc8-122">**刪除**</span><span class="sxs-lookup"><span data-stu-id="9afc8-122">**Delete**</span></span>](itmediacollection-delete.md)                        | <span data-ttu-id="9afc8-123">刪除對應至指定之索引的媒體。</span><span class="sxs-lookup"><span data-stu-id="9afc8-123">Deletes the media corresponding to the specified index.</span></span><br/>     |
| [<span data-ttu-id="9afc8-124">**取得 \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="9afc8-124">**get\_\_NewEnum**</span></span>](itmediacollection-get--newenum.md)          | <span data-ttu-id="9afc8-125">傳回集合的列舉程式。</span><span class="sxs-lookup"><span data-stu-id="9afc8-125">Returns an enumerator for the collection.</span></span><br/>                   |
| [<span data-ttu-id="9afc8-126">**取得 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="9afc8-126">**get\_Count**</span></span>](itmediacollection-get-count.md)                 | <span data-ttu-id="9afc8-127">取得會話中的媒體數目。</span><span class="sxs-lookup"><span data-stu-id="9afc8-127">Gets the number of media in the session.</span></span><br/>                    |
| [<span data-ttu-id="9afc8-128">**取得 \_ EnumerationIf**</span><span class="sxs-lookup"><span data-stu-id="9afc8-128">**get\_EnumerationIf**</span></span>](itmediacollection-get-enumerationif.md) | <span data-ttu-id="9afc8-129">取得列舉介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9afc8-129">Gets pointer to enumeration interface.</span></span><br/>                      |
| [<span data-ttu-id="9afc8-130">**取得 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="9afc8-130">**get\_Item**</span></span>](itmediacollection-get-item.md)                   | <span data-ttu-id="9afc8-131">傳回對應至指定之索引的媒體。</span><span class="sxs-lookup"><span data-stu-id="9afc8-131">Returns the media corresponding to the specified index.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="9afc8-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="9afc8-132">Requirements</span></span>



| <span data-ttu-id="9afc8-133">需求</span><span class="sxs-lookup"><span data-stu-id="9afc8-133">Requirement</span></span> | <span data-ttu-id="9afc8-134">值</span><span class="sxs-lookup"><span data-stu-id="9afc8-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9afc8-135">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="9afc8-135">TAPI version</span></span><br/> | <span data-ttu-id="9afc8-136">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9afc8-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9afc8-137">標頭</span><span class="sxs-lookup"><span data-stu-id="9afc8-137">Header</span></span><br/>       | <dl> <span data-ttu-id="9afc8-138"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="9afc8-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9afc8-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="9afc8-139">Library</span></span><br/>      | <dl> <span data-ttu-id="9afc8-140"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="9afc8-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9afc8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9afc8-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="9afc8-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9afc8-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



 


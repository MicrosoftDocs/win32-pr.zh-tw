---
description: IEnumTime 介面會為 ITTime 介面提供 COM 標準的列舉方法。 ITTimeCollection：： get \_ EnumerationIf 方法會將指標傳回至 IEnumTime。
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: 'IEnumTime 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977745"
---
# <a name="ienumtime-interface"></a><span data-ttu-id="fd046-104">IEnumTime 介面</span><span class="sxs-lookup"><span data-stu-id="fd046-104">IEnumTime interface</span></span>

<span data-ttu-id="fd046-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="fd046-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fd046-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="fd046-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fd046-107">**IEnumTime** 介面會為 [**ITTIME**](ittime.md)介面提供 COM 標準的列舉方法。</span><span class="sxs-lookup"><span data-stu-id="fd046-107">The **IEnumTime** interface provides COM-standard enumeration methods for the [**ITTime**](ittime.md) interface.</span></span> <span data-ttu-id="fd046-108">[**ITTimeCollection：： get \_ EnumerationIf**](ittimecollection-get-enumerationif.md)方法會將指標傳回至 **IEnumTime**。</span><span class="sxs-lookup"><span data-stu-id="fd046-108">The [**ITTimeCollection::get\_EnumerationIf**](ittimecollection-get-enumerationif.md) method returns a pointer to **IEnumTime**.</span></span>

## <a name="members"></a><span data-ttu-id="fd046-109">成員</span><span class="sxs-lookup"><span data-stu-id="fd046-109">Members</span></span>

<span data-ttu-id="fd046-110">**IEnumTime** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="fd046-110">The **IEnumTime** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fd046-111">**IEnumTime** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fd046-111">**IEnumTime** also has these types of members:</span></span>

-   [<span data-ttu-id="fd046-112">方法</span><span class="sxs-lookup"><span data-stu-id="fd046-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fd046-113">方法</span><span class="sxs-lookup"><span data-stu-id="fd046-113">Methods</span></span>

<span data-ttu-id="fd046-114">**IEnumTime** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fd046-114">The **IEnumTime** interface has these methods.</span></span>



| <span data-ttu-id="fd046-115">方法</span><span class="sxs-lookup"><span data-stu-id="fd046-115">Method</span></span>                           | <span data-ttu-id="fd046-116">描述</span><span class="sxs-lookup"><span data-stu-id="fd046-116">Description</span></span>                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd046-117">**克隆**</span><span class="sxs-lookup"><span data-stu-id="fd046-117">**Clone**</span></span>](ienumtime-clone.md) | <span data-ttu-id="fd046-118">建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。</span><span class="sxs-lookup"><span data-stu-id="fd046-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="fd046-119">**下一步**</span><span class="sxs-lookup"><span data-stu-id="fd046-119">**Next**</span></span>](ienumtime-next.md)   | <span data-ttu-id="fd046-120">取得列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="fd046-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="fd046-121">**重設**</span><span class="sxs-lookup"><span data-stu-id="fd046-121">**Reset**</span></span>](ienumtime-reset.md) | <span data-ttu-id="fd046-122">重設為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="fd046-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="fd046-123">**跳過**</span><span class="sxs-lookup"><span data-stu-id="fd046-123">**Skip**</span></span>](ienumtime-skip.md)   | <span data-ttu-id="fd046-124">略過列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="fd046-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="fd046-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd046-125">Requirements</span></span>



| <span data-ttu-id="fd046-126">需求</span><span class="sxs-lookup"><span data-stu-id="fd046-126">Requirement</span></span> | <span data-ttu-id="fd046-127">值</span><span class="sxs-lookup"><span data-stu-id="fd046-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd046-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="fd046-128">TAPI version</span></span><br/> | <span data-ttu-id="fd046-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="fd046-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fd046-130">標頭</span><span class="sxs-lookup"><span data-stu-id="fd046-130">Header</span></span><br/>       | <dl> <span data-ttu-id="fd046-131"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd046-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd046-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="fd046-132">Library</span></span><br/>      | <dl> <span data-ttu-id="fd046-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="fd046-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fd046-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fd046-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="fd046-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd046-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 


---
description: IEnumMedia 介面會為 ITMedia 介面提供 COM 標準的列舉方法。 ITMediaCollection：： get \_ EnumerationIf 方法會將指標傳回至 IEnumMedia。
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: 'IEnumMedia 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994886"
---
# <a name="ienummedia-interface"></a><span data-ttu-id="f90b1-104">IEnumMedia 介面</span><span class="sxs-lookup"><span data-stu-id="f90b1-104">IEnumMedia interface</span></span>

<span data-ttu-id="f90b1-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="f90b1-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f90b1-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f90b1-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f90b1-107">**IEnumMedia** 介面會為 [**ITMEDIA**](itmedia.md)介面提供 COM 標準的列舉方法。</span><span class="sxs-lookup"><span data-stu-id="f90b1-107">The **IEnumMedia** interface provides COM-standard enumeration methods for the [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="f90b1-108">[**ITMediaCollection：： get \_ EnumerationIf**](itmediacollection-get-enumerationif.md)方法會將指標傳回至 **IEnumMedia**。</span><span class="sxs-lookup"><span data-stu-id="f90b1-108">The [**ITMediaCollection::get\_EnumerationIf**](itmediacollection-get-enumerationif.md) method returns a pointer to **IEnumMedia**.</span></span>

## <a name="members"></a><span data-ttu-id="f90b1-109">成員</span><span class="sxs-lookup"><span data-stu-id="f90b1-109">Members</span></span>

<span data-ttu-id="f90b1-110">**IEnumMedia** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="f90b1-110">The **IEnumMedia** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f90b1-111">**IEnumMedia** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f90b1-111">**IEnumMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="f90b1-112">方法</span><span class="sxs-lookup"><span data-stu-id="f90b1-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f90b1-113">方法</span><span class="sxs-lookup"><span data-stu-id="f90b1-113">Methods</span></span>

<span data-ttu-id="f90b1-114">**IEnumMedia** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f90b1-114">The **IEnumMedia** interface has these methods.</span></span>



| <span data-ttu-id="f90b1-115">方法</span><span class="sxs-lookup"><span data-stu-id="f90b1-115">Method</span></span>                            | <span data-ttu-id="f90b1-116">描述</span><span class="sxs-lookup"><span data-stu-id="f90b1-116">Description</span></span>                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f90b1-117">**克隆**</span><span class="sxs-lookup"><span data-stu-id="f90b1-117">**Clone**</span></span>](ienummedia-clone.md) | <span data-ttu-id="f90b1-118">建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。</span><span class="sxs-lookup"><span data-stu-id="f90b1-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="f90b1-119">**下一步**</span><span class="sxs-lookup"><span data-stu-id="f90b1-119">**Next**</span></span>](ienummedia-next.md)   | <span data-ttu-id="f90b1-120">取得列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="f90b1-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="f90b1-121">**重設**</span><span class="sxs-lookup"><span data-stu-id="f90b1-121">**Reset**</span></span>](ienummedia-reset.md) | <span data-ttu-id="f90b1-122">重設為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="f90b1-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="f90b1-123">**跳過**</span><span class="sxs-lookup"><span data-stu-id="f90b1-123">**Skip**</span></span>](ienummedia-skip.md)   | <span data-ttu-id="f90b1-124">略過列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="f90b1-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="f90b1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f90b1-125">Requirements</span></span>



| <span data-ttu-id="f90b1-126">需求</span><span class="sxs-lookup"><span data-stu-id="f90b1-126">Requirement</span></span> | <span data-ttu-id="f90b1-127">值</span><span class="sxs-lookup"><span data-stu-id="f90b1-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f90b1-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f90b1-128">TAPI version</span></span><br/> | <span data-ttu-id="f90b1-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f90b1-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f90b1-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f90b1-130">Header</span></span><br/>       | <dl> <span data-ttu-id="f90b1-131"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="f90b1-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f90b1-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="f90b1-132">Library</span></span><br/>      | <dl> <span data-ttu-id="f90b1-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="f90b1-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f90b1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f90b1-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="f90b1-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f90b1-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 


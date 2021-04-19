---
description: IEnumParticipant 介面會為 ITParticipant 介面提供 COM 標準的列舉方法。 ITParticipantControl：： EnumerateParticipants 方法會將指標傳回至 IEnumParticipant。
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: 'IEnumParticipant 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981382"
---
# <a name="ienumparticipant-interface"></a><span data-ttu-id="0209d-104">IEnumParticipant 介面</span><span class="sxs-lookup"><span data-stu-id="0209d-104">IEnumParticipant interface</span></span>

<span data-ttu-id="0209d-105">\[**IEnumParticipant** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="0209d-105">\[**IEnumParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0209d-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="0209d-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0209d-107">**IEnumParticipant** 介面會為 [**ITPARTICIPANT**](itparticipant.md)介面提供 COM 標準的列舉方法。</span><span class="sxs-lookup"><span data-stu-id="0209d-107">The **IEnumParticipant** interface provides COM-standard enumeration methods for the [**ITParticipant**](itparticipant.md) interface.</span></span> <span data-ttu-id="0209d-108">[**ITParticipantControl：： EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md)方法會將指標傳回至 **IEnumParticipant**。</span><span class="sxs-lookup"><span data-stu-id="0209d-108">The [**ITParticipantControl::EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method returns a pointer to **IEnumParticipant**.</span></span>

<span data-ttu-id="0209d-109">Visual Basic 和指令碼語言都隱藏了 **IEnumParticipant** 介面。</span><span class="sxs-lookup"><span data-stu-id="0209d-109">The **IEnumParticipant** interface is hidden from Visual Basic and scripting languages.</span></span>

## <a name="members"></a><span data-ttu-id="0209d-110">成員</span><span class="sxs-lookup"><span data-stu-id="0209d-110">Members</span></span>

<span data-ttu-id="0209d-111">**IEnumParticipant** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="0209d-111">The **IEnumParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0209d-112">**IEnumParticipant** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0209d-112">**IEnumParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="0209d-113">方法</span><span class="sxs-lookup"><span data-stu-id="0209d-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0209d-114">方法</span><span class="sxs-lookup"><span data-stu-id="0209d-114">Methods</span></span>

<span data-ttu-id="0209d-115">**IEnumParticipant** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0209d-115">The **IEnumParticipant** interface has these methods.</span></span>



| <span data-ttu-id="0209d-116">方法</span><span class="sxs-lookup"><span data-stu-id="0209d-116">Method</span></span>                                  | <span data-ttu-id="0209d-117">描述</span><span class="sxs-lookup"><span data-stu-id="0209d-117">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0209d-118">**克隆**</span><span class="sxs-lookup"><span data-stu-id="0209d-118">**Clone**</span></span>](ienumparticipant-clone.md) | <span data-ttu-id="0209d-119">建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。</span><span class="sxs-lookup"><span data-stu-id="0209d-119">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="0209d-120">**下一步**</span><span class="sxs-lookup"><span data-stu-id="0209d-120">**Next**</span></span>](ienumparticipant-next.md)   | <span data-ttu-id="0209d-121">取得列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="0209d-121">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="0209d-122">**重設**</span><span class="sxs-lookup"><span data-stu-id="0209d-122">**Reset**</span></span>](ienumparticipant-reset.md) | <span data-ttu-id="0209d-123">重設為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="0209d-123">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="0209d-124">**跳過**</span><span class="sxs-lookup"><span data-stu-id="0209d-124">**Skip**</span></span>](ienumparticipant-skip.md)   | <span data-ttu-id="0209d-125">略過列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="0209d-125">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="0209d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="0209d-126">Requirements</span></span>



| <span data-ttu-id="0209d-127">需求</span><span class="sxs-lookup"><span data-stu-id="0209d-127">Requirement</span></span> | <span data-ttu-id="0209d-128">值</span><span class="sxs-lookup"><span data-stu-id="0209d-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0209d-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="0209d-129">TAPI version</span></span><br/> | <span data-ttu-id="0209d-130">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0209d-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0209d-131">標頭</span><span class="sxs-lookup"><span data-stu-id="0209d-131">Header</span></span><br/>       | <dl> <span data-ttu-id="0209d-132"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="0209d-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="0209d-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="0209d-133">Library</span></span><br/>      | <dl> <span data-ttu-id="0209d-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="0209d-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0209d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0209d-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="0209d-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0209d-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0209d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0209d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0209d-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="0209d-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 


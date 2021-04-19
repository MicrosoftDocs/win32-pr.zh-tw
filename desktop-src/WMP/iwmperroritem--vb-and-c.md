---
title: 'IWMPErrorItem (VB 和 C ) 介面 (h.264. h) '
description: 提供錯誤資訊的存取。
ms.assetid: 7f1571e1-4e3a-4f06-b9fa-9add34266537
keywords:
- IWMPErrorItem (VB 和 C ) 介面 Windows Media Player
- IWMPErrorItem (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPErrorItem (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65864900e16cf1b4309677ba89e7d5f1eca84442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000834"
---
# <a name="iwmperroritem-vb-and-c-interface"></a><span data-ttu-id="b57d4-105">IWMPErrorItem (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="b57d4-105">IWMPErrorItem (VB and C#) interface</span></span>

<span data-ttu-id="b57d4-106">提供錯誤資訊的存取。</span><span class="sxs-lookup"><span data-stu-id="b57d4-106">Provides access to error information.</span></span>

<span data-ttu-id="b57d4-107">**IWMPErrorItem** 介面會公開下列屬性。</span><span class="sxs-lookup"><span data-stu-id="b57d4-107">The **IWMPErrorItem** interface exposes the following properties.</span></span>



| <span data-ttu-id="b57d4-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b57d4-108">Property</span></span>                                                                             | <span data-ttu-id="b57d4-109">描述</span><span class="sxs-lookup"><span data-stu-id="b57d4-109">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b57d4-110">customUrl</span><span class="sxs-lookup"><span data-stu-id="b57d4-110">customUrl</span></span>](wmplibiwmperroritem-iwmperroritem-customurl--vb-and-c.md)               | <span data-ttu-id="b57d4-111">取得網站的 URL，這個網站會顯示有關編解碼器下載失敗的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="b57d4-111">Gets the URL of a website that displays specific information about codec download failure.</span></span> |
| [<span data-ttu-id="b57d4-112">errorCode</span><span class="sxs-lookup"><span data-stu-id="b57d4-112">errorCode</span></span>](wmplibiwmperroritem-iwmperroritem-errorcode--vb-and-c.md)               | <span data-ttu-id="b57d4-113">取得目前的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b57d4-113">Gets the current error code.</span></span>                                                               |
| [<span data-ttu-id="b57d4-114">errorCoNtext</span><span class="sxs-lookup"><span data-stu-id="b57d4-114">errorContext</span></span>](wmplibiwmperroritem-iwmperroritem-errorcontext--vb-and-c.md)         | <span data-ttu-id="b57d4-115">取得值，指出錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="b57d4-115">Gets a value indicating the context of the error.</span></span>                                          |
| [<span data-ttu-id="b57d4-116">errorDescription</span><span class="sxs-lookup"><span data-stu-id="b57d4-116">errorDescription</span></span>](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md) | <span data-ttu-id="b57d4-117">取得錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="b57d4-117">Gets a description of the error.</span></span>                                                           |
| [<span data-ttu-id="b57d4-118">補救</span><span class="sxs-lookup"><span data-stu-id="b57d4-118">remedy</span></span>](wmplibiwmperroritem-iwmperroritem-remedy--vb-and-c.md)                     | <span data-ttu-id="b57d4-119">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="b57d4-119">Reserved for future use.</span></span>                                                                   |



 

<span data-ttu-id="b57d4-120">使用下列屬性取得 **IWMPErrorItem** 介面。</span><span class="sxs-lookup"><span data-stu-id="b57d4-120">Get an **IWMPErrorItem** interface using the following property.</span></span>



| <span data-ttu-id="b57d4-121">介面</span><span class="sxs-lookup"><span data-stu-id="b57d4-121">Interface</span></span>                            | <span data-ttu-id="b57d4-122">屬性</span><span class="sxs-lookup"><span data-stu-id="b57d4-122">Property</span></span>                                                                   |
|--------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="b57d4-123">IWMPError</span><span class="sxs-lookup"><span data-stu-id="b57d4-123">IWMPError</span></span>](iwmperror--vb-and-c.md) | <span data-ttu-id="b57d4-124">C # 中的 [專案](iwmperror-item--vb-and-c.md) (使用 **取得 \_ 專案** 方法) </span><span class="sxs-lookup"><span data-stu-id="b57d4-124">[Item](iwmperror-item--vb-and-c.md) (in C# use the **get\_Item** method)</span></span> |



 

## <a name="members"></a><span data-ttu-id="b57d4-125">成員</span><span class="sxs-lookup"><span data-stu-id="b57d4-125">Members</span></span>

<span data-ttu-id="b57d4-126">**IWMPErrorItem (VB 和 c # )** 介面不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="b57d4-126">The **IWMPErrorItem (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="b57d4-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b57d4-127">Requirements</span></span>



| <span data-ttu-id="b57d4-128">需求</span><span class="sxs-lookup"><span data-stu-id="b57d4-128">Requirement</span></span> | <span data-ttu-id="b57d4-129">值</span><span class="sxs-lookup"><span data-stu-id="b57d4-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b57d4-130">標頭</span><span class="sxs-lookup"><span data-stu-id="b57d4-130">Header</span></span><br/> | <dl> <span data-ttu-id="b57d4-131"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b57d4-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b57d4-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b57d4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b57d4-133">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="b57d4-133">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="b57d4-134">**IWMPErrorItem2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b57d4-134">**IWMPErrorItem2 Interface (VB and C#)**</span></span>](iwmperroritem2--vb-and-c.md)
</dt> </dl>

 

 






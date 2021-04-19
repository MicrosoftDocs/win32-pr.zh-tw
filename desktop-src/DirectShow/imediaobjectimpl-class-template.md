---
description: IMediaObjectImpl 類別範本提供 IMediaObject 介面的基底實作為基底。 如需使用此範本的詳細資訊，請參閱使用 SQL-DMO 類別範本。
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: 'IMediaObjectImpl 類別範本 (Dmoimpl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990070"
---
# <a name="imediaobjectimpl-class-template"></a><span data-ttu-id="1a57c-104">IMediaObjectImpl 類別範本</span><span class="sxs-lookup"><span data-stu-id="1a57c-104">IMediaObjectImpl Class Template</span></span>

<span data-ttu-id="1a57c-105">`IMediaObjectImpl`類別樣板提供 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)介面的基底實作為基底。</span><span class="sxs-lookup"><span data-stu-id="1a57c-105">The `IMediaObjectImpl` class template provides a base implementation for the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="1a57c-106">如需使用此範本的詳細資訊，請參閱 [使用 Sql-dmo 類別範本](using-the-dmo-class-template.md)。</span><span class="sxs-lookup"><span data-stu-id="1a57c-106">For more information on using this template, see [Using the DMO Class Template](using-the-dmo-class-template.md).</span></span>

<span data-ttu-id="1a57c-107">此 `IMediaObjectImpl` 範本會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="1a57c-107">This `IMediaObjectImpl` template exposes the following members.</span></span>



| <span data-ttu-id="1a57c-108">Nested 類別</span><span class="sxs-lookup"><span data-stu-id="1a57c-108">Nested Class</span></span>                              | <span data-ttu-id="1a57c-109">Description</span><span class="sxs-lookup"><span data-stu-id="1a57c-109">Description</span></span>                                  |
|-------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="1a57c-110">**LockIt**</span><span class="sxs-lookup"><span data-stu-id="1a57c-110">**LockIt**</span></span>](imediaobjectimpl-lockit.md) | <span data-ttu-id="1a57c-111">鎖定和解除鎖定的 Helper 類別。</span><span class="sxs-lookup"><span data-stu-id="1a57c-111">Helper class that locks and unlocks the DMO.</span></span> |



 



| <span data-ttu-id="1a57c-112">方法</span><span class="sxs-lookup"><span data-stu-id="1a57c-112">Method</span></span>                                                                      | <span data-ttu-id="1a57c-113">描述</span><span class="sxs-lookup"><span data-stu-id="1a57c-113">Description</span></span>                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="1a57c-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1a57c-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span></span>                     | <span data-ttu-id="1a57c-115">判斷所有非選用的資料流程是否都有媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1a57c-115">Determines whether all of the non-optional streams have media types.</span></span> |
| <span data-ttu-id="1a57c-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1a57c-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span></span>                             | <span data-ttu-id="1a57c-117">抓取指定輸入資料流程目前的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1a57c-117">Retrieves the current media type for a specified input stream.</span></span>       |
| <span data-ttu-id="1a57c-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1a57c-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span></span>                       | <span data-ttu-id="1a57c-119">查詢是否在輸入資料流程上設定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1a57c-119">Queries whether the media type was set on an input stream.</span></span>           |
| <span data-ttu-id="1a57c-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1a57c-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span></span>   | <span data-ttu-id="1a57c-121">查詢輸入資料流程是否可以接受更多輸入。</span><span class="sxs-lookup"><span data-stu-id="1a57c-121">Queries whether an input stream can accept more input.</span></span>               |
| <span data-ttu-id="1a57c-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1a57c-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span></span>   | <span data-ttu-id="1a57c-123">查詢輸入資料流程是否可以接受指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1a57c-123">Queries whether an input stream can accept a given media type.</span></span>       |
| <span data-ttu-id="1a57c-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1a57c-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span></span> | <span data-ttu-id="1a57c-125">查詢輸出資料流程是否可以接受指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1a57c-125">Queries whether an output stream can accept a given media type.</span></span>      |
| <span data-ttu-id="1a57c-126">[**鎖定**](/previous-versions/ms809100(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1a57c-126">[**Lock**](/previous-versions/ms809100(v=msdn.10))</span></span>                                       | <span data-ttu-id="1a57c-127">鎖定</span><span class="sxs-lookup"><span data-stu-id="1a57c-127">Locks the DMO</span></span>                                                        |
| <span data-ttu-id="1a57c-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1a57c-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span></span>                           | <span data-ttu-id="1a57c-129">抓取指定輸出資料流程目前的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1a57c-129">Retrieves the current media type for a specified output stream.</span></span>      |
| <span data-ttu-id="1a57c-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1a57c-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span></span>                     | <span data-ttu-id="1a57c-131">查詢是否在輸出資料流程上設定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1a57c-131">Queries whether the media type was set on an output stream.</span></span>          |
| <span data-ttu-id="1a57c-132">[**Unlock**](/previous-versions/ms809101(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1a57c-132">[**Unlock**](/previous-versions/ms809101(v=msdn.10))</span></span>                                   | <span data-ttu-id="1a57c-133">解除鎖定</span><span class="sxs-lookup"><span data-stu-id="1a57c-133">Unlocks the DMO</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="1a57c-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a57c-134">Requirements</span></span>



| <span data-ttu-id="1a57c-135">需求</span><span class="sxs-lookup"><span data-stu-id="1a57c-135">Requirement</span></span> | <span data-ttu-id="1a57c-136">值</span><span class="sxs-lookup"><span data-stu-id="1a57c-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a57c-137">標頭</span><span class="sxs-lookup"><span data-stu-id="1a57c-137">Header</span></span><br/>  | <dl> <span data-ttu-id="1a57c-138"><dt>Dmoimpl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a57c-138"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="1a57c-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="1a57c-139">Library</span></span><br/> | <dl> <span data-ttu-id="1a57c-140"><dt>Dmoguids .lib;</dt><dt>Msdmo .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a57c-140"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a57c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a57c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a57c-142">SQL-DMO 參考</span><span class="sxs-lookup"><span data-stu-id="1a57c-142">DMO Reference</span></span>](dmo-reference.md)
</dt> <dt>

[<span data-ttu-id="1a57c-143">使用 SQL-DMO 類別範本</span><span class="sxs-lookup"><span data-stu-id="1a57c-143">Using the DMO Class Template</span></span>](using-the-dmo-class-template.md)
</dt> </dl>

 

 

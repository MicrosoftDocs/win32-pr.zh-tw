---
description: 下表包含適用于 Microsoft DirectX 媒體物件 (DMOs) 的錯誤碼。 這些錯誤碼會定義在標頭檔 Mediaerr 中。
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: 'SQL-DMO 錯誤碼 (Mediaerr .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984436"
---
# <a name="dmo-error-codes"></a><span data-ttu-id="07842-104">SQL-DMO 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="07842-104">DMO Error Codes</span></span>

<span data-ttu-id="07842-105">下表包含適用于 Microsoft DirectX 媒體物件 (DMOs) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="07842-105">The following table contains error codes that are specific to Microsoft DirectX Media Objects (DMOs).</span></span> <span data-ttu-id="07842-106">這些錯誤碼會定義在標頭檔 Mediaerr 中。</span><span class="sxs-lookup"><span data-stu-id="07842-106">These error codes are defined in the header file Mediaerr.h.</span></span>



| <span data-ttu-id="07842-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="07842-107">Constant/value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="07842-108">Description</span><span class="sxs-lookup"><span data-stu-id="07842-108">Description</span></span>                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <span data-ttu-id="07842-109"><dt>**Sql-dmo \_E \_ INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="07842-109"><dt>**DMO\_E\_INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span></span> </dl> | <span data-ttu-id="07842-110">不正確資料流程索引。</span><span class="sxs-lookup"><span data-stu-id="07842-110">Invalid stream index.</span></span><br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <span data-ttu-id="07842-111"><dt>**Sql-dmo \_E \_ INVALIDTYPE**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="07842-111"><dt>**DMO\_E\_INVALIDTYPE**</dt> <dt>0x80040202</dt></span></span> </dl>                      | <span data-ttu-id="07842-112">媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="07842-112">Invalid media type.</span></span><br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <span data-ttu-id="07842-113"><dt>**Sql-dmo \_E \_ 類型 \_ 未 \_ 設定**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="07842-113"><dt>**DMO\_E\_TYPE\_NOT\_SET**</dt> <dt>0x80040203</dt></span></span> </dl>                 | <span data-ttu-id="07842-114">媒體類型未設定。</span><span class="sxs-lookup"><span data-stu-id="07842-114">Media type was not set.</span></span> <span data-ttu-id="07842-115">一或多個資料流程需要媒體類型，才能執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="07842-115">One or more streams require a media type before this operation can be performed.</span></span><br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <span data-ttu-id="07842-116"><dt>**Sql-dmo \_E \_ NOTACCEPTING**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="07842-116"><dt>**DMO\_E\_NOTACCEPTING**</dt> <dt>0x80040204</dt></span></span> </dl>                   | <span data-ttu-id="07842-117">此資料流程無法接受資料。</span><span class="sxs-lookup"><span data-stu-id="07842-117">Data cannot be accepted on this stream.</span></span> <span data-ttu-id="07842-118">您可能需要處理更多輸出資料;請參閱 [**IMediaObject：:P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput)。</span><span class="sxs-lookup"><span data-stu-id="07842-118">You might need to process more output data; see [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span></span><br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <span data-ttu-id="07842-119"><dt>**Sql-dmo \_E \_ 類型 \_ 不 \_ 接受**</dt> <dt>0x80040205</dt></span><span class="sxs-lookup"><span data-stu-id="07842-119"><dt>**DMO\_E\_TYPE\_NOT\_ACCEPTED**</dt> <dt>0x80040205</dt></span></span> </dl>  | <span data-ttu-id="07842-120">媒體類型不被接受。</span><span class="sxs-lookup"><span data-stu-id="07842-120">Media type was not accepted.</span></span><br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <span data-ttu-id="07842-121"><dt>**Sql-dmo \_\_沒有 \_ 其他 \_ 專案**</dt> <dt>0x80040206</dt></span><span class="sxs-lookup"><span data-stu-id="07842-121"><dt>**DMO\_E\_NO\_MORE\_ITEMS**</dt> <dt>0x80040206</dt></span></span> </dl>              | <span data-ttu-id="07842-122">媒體類型索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="07842-122">Media-type index is out of range.</span></span><br/>                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="07842-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="07842-123">Requirements</span></span>



| <span data-ttu-id="07842-124">需求</span><span class="sxs-lookup"><span data-stu-id="07842-124">Requirement</span></span> | <span data-ttu-id="07842-125">值</span><span class="sxs-lookup"><span data-stu-id="07842-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07842-126">標頭</span><span class="sxs-lookup"><span data-stu-id="07842-126">Header</span></span><br/> | <dl> <span data-ttu-id="07842-127"><dt>Mediaerr。h</dt></span><span class="sxs-lookup"><span data-stu-id="07842-127"><dt>Mediaerr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07842-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07842-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07842-129">SQL-DMO 常數</span><span class="sxs-lookup"><span data-stu-id="07842-129">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 





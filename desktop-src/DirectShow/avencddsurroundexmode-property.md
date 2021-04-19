---
description: 指定杜比數位音訊資料流程是否以杜數位環繞（例如）編碼。 此屬性適用于杜比數位音訊編碼器。
ms.assetid: bc74a002-ef9a-4cb3-a999-cb7a0481e132
title: 'AVEncDDSurroundExMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95facf9759661d83f7e46e7d3436e6b165518a80
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973747"
---
# <a name="avencddsurroundexmode-property"></a><span data-ttu-id="3dbcb-104">AVEncDDSurroundExMode 屬性</span><span class="sxs-lookup"><span data-stu-id="3dbcb-104">AVEncDDSurroundExMode property</span></span>

<span data-ttu-id="3dbcb-105">指定杜比數位音訊資料流程是否以杜數位環繞（例如）編碼。</span><span class="sxs-lookup"><span data-stu-id="3dbcb-105">Specifies whether a Dolby Digital audio stream is encoded in Dolby Digital Surround EX.</span></span> <span data-ttu-id="3dbcb-106">此屬性適用于杜比數位音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="3dbcb-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="3dbcb-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="3dbcb-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="3dbcb-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="3dbcb-108">Data type</span></span>

<span data-ttu-id="3dbcb-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="3dbcb-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3dbcb-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="3dbcb-110">Property GUID</span></span>

<span data-ttu-id="3dbcb-111">**CODECAPI \_ AVEncDDSurroundExMode**</span><span class="sxs-lookup"><span data-stu-id="3dbcb-111">**CODECAPI\_AVEncDDSurroundExMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="3dbcb-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="3dbcb-112">Property value</span></span>

<span data-ttu-id="3dbcb-113">這個屬性的值是 [**eAVEncDDSurroundExMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddsurroundexmode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="3dbcb-113">The value of this property is a member of the [**eAVEncDDSurroundExMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddsurroundexmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dbcb-114">備註</span><span class="sxs-lookup"><span data-stu-id="3dbcb-114">Remarks</span></span>

<span data-ttu-id="3dbcb-115">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="3dbcb-115">This property is read/write.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dbcb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3dbcb-116">Requirements</span></span>



| <span data-ttu-id="3dbcb-117">需求</span><span class="sxs-lookup"><span data-stu-id="3dbcb-117">Requirement</span></span> | <span data-ttu-id="3dbcb-118">值</span><span class="sxs-lookup"><span data-stu-id="3dbcb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3dbcb-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3dbcb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3dbcb-120">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3dbcb-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3dbcb-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3dbcb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3dbcb-122">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3dbcb-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3dbcb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3dbcb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dbcb-124"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3dbcb-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dbcb-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3dbcb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dbcb-126">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="3dbcb-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="3dbcb-127">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="3dbcb-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 





---
description: 指定您想要用於影片編碼的裝置一致性範本。
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: 'MFPKEY_DECODERCOMPLEXITYREQUESTED 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980799"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a><span data-ttu-id="016c7-103">MFPKEY \_ DECODERCOMPLEXITYREQUESTED 屬性</span><span class="sxs-lookup"><span data-stu-id="016c7-103">MFPKEY\_DECODERCOMPLEXITYREQUESTED Property</span></span>

<span data-ttu-id="016c7-104">指定您想要用於影片編碼的裝置一致性範本。</span><span class="sxs-lookup"><span data-stu-id="016c7-104">Specifies the device conformance template that you want to use for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="016c7-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="016c7-105">Data Type</span></span>

<span data-ttu-id="016c7-106">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="016c7-106">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="016c7-107">預設值</span><span class="sxs-lookup"><span data-stu-id="016c7-107">Default Value</span></span>

<span data-ttu-id="016c7-108">1</span><span class="sxs-lookup"><span data-stu-id="016c7-108">1</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="016c7-109">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="016c7-109">Constant for IPropertyBag</span></span>

<span data-ttu-id="016c7-110">g \_ wszWMVCDecoderComplexityRequested</span><span class="sxs-lookup"><span data-stu-id="016c7-110">g\_wszWMVCDecoderComplexityRequested</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="016c7-111">IPropertyBag 的資料類型</span><span class="sxs-lookup"><span data-stu-id="016c7-111">Data Type for IPropertyBag</span></span>

<span data-ttu-id="016c7-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="016c7-112">VT\_BSTR</span></span>

## <a name="default-value-for-ipropertybag"></a><span data-ttu-id="016c7-113">IPropertyBag 的預設值</span><span class="sxs-lookup"><span data-stu-id="016c7-113">Default Value for IPropertyBag</span></span>

<span data-ttu-id="016c7-114">多功能</span><span class="sxs-lookup"><span data-stu-id="016c7-114">"MP"</span></span>

## <a name="remarks"></a><span data-ttu-id="016c7-115">備註</span><span class="sxs-lookup"><span data-stu-id="016c7-115">Remarks</span></span>

<span data-ttu-id="016c7-116">編解碼器將嘗試使用此值指定的裝置一致性範本來編碼內容。</span><span class="sxs-lookup"><span data-stu-id="016c7-116">The codec will attempt to encode the content using the device conformance template specified by this value.</span></span> <span data-ttu-id="016c7-117">編碼之後，您可以從 [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) 屬性中取出編碼內容符合的實際範本。</span><span class="sxs-lookup"><span data-stu-id="016c7-117">The actual template to which the encoded content conforms can be retrieved from the [MFPKEY\_DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) property after encoding.</span></span>

<span data-ttu-id="016c7-118">這個屬性必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="016c7-118">This property must be one of the following values.</span></span>



| <span data-ttu-id="016c7-119">IPropertyStore 的值</span><span class="sxs-lookup"><span data-stu-id="016c7-119">Value for IPropertyStore</span></span> | <span data-ttu-id="016c7-120">IPropertyBag 的值</span><span class="sxs-lookup"><span data-stu-id="016c7-120">Value for IPropertyBag</span></span> | <span data-ttu-id="016c7-121">描述</span><span class="sxs-lookup"><span data-stu-id="016c7-121">Description</span></span>         |
|--------------------------|------------------------|---------------------|
| <span data-ttu-id="016c7-122">0</span><span class="sxs-lookup"><span data-stu-id="016c7-122">0</span></span>                        | <span data-ttu-id="016c7-123">SP-1</span><span class="sxs-lookup"><span data-stu-id="016c7-123">"SP"</span></span>                   | <span data-ttu-id="016c7-124">簡單設定檔</span><span class="sxs-lookup"><span data-stu-id="016c7-124">simple profile</span></span>      |
| <span data-ttu-id="016c7-125">1</span><span class="sxs-lookup"><span data-stu-id="016c7-125">1</span></span>                        | <span data-ttu-id="016c7-126">多功能</span><span class="sxs-lookup"><span data-stu-id="016c7-126">"MP"</span></span>                   | <span data-ttu-id="016c7-127">主要設定檔</span><span class="sxs-lookup"><span data-stu-id="016c7-127">main profile</span></span>        |
| <span data-ttu-id="016c7-128">2</span><span class="sxs-lookup"><span data-stu-id="016c7-128">2</span></span>                        | <span data-ttu-id="016c7-129">CP</span><span class="sxs-lookup"><span data-stu-id="016c7-129">"CP"</span></span>                   | <span data-ttu-id="016c7-130">不再支援</span><span class="sxs-lookup"><span data-stu-id="016c7-130">no longer supported</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="016c7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="016c7-131">Requirements</span></span>



| <span data-ttu-id="016c7-132">需求</span><span class="sxs-lookup"><span data-stu-id="016c7-132">Requirement</span></span> | <span data-ttu-id="016c7-133">值</span><span class="sxs-lookup"><span data-stu-id="016c7-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="016c7-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="016c7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="016c7-135">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="016c7-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="016c7-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="016c7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="016c7-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="016c7-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="016c7-138">標頭</span><span class="sxs-lookup"><span data-stu-id="016c7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="016c7-139"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="016c7-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="016c7-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="016c7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="016c7-141">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="016c7-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 





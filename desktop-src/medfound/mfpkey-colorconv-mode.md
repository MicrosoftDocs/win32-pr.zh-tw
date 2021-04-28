---
description: MFPKEY_COLORCONV_MODE 屬性-指定輸入資料流程是否為交錯式。
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: 'MFPKEY_COLORCONV_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3f2d6256c4d7a9410264fb18703eea251e9c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087576"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="08c18-103">MFPKEY \_ COLORCONV \_ MODE 屬性</span><span class="sxs-lookup"><span data-stu-id="08c18-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="08c18-104">指定輸入資料流程是否為交錯式。</span><span class="sxs-lookup"><span data-stu-id="08c18-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="08c18-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="08c18-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="08c18-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="08c18-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="08c18-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="08c18-107">Data Type</span></span>

<span data-ttu-id="08c18-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="08c18-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="08c18-109">預設值</span><span class="sxs-lookup"><span data-stu-id="08c18-109">Default Value</span></span>

<span data-ttu-id="08c18-110">由來自來源影片的 DSP 所計算。</span><span class="sxs-lookup"><span data-stu-id="08c18-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="08c18-111">套用至</span><span class="sxs-lookup"><span data-stu-id="08c18-111">Applies To</span></span>

-   [<span data-ttu-id="08c18-112">色彩轉換器 DSP</span><span class="sxs-lookup"><span data-stu-id="08c18-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="08c18-113">備註</span><span class="sxs-lookup"><span data-stu-id="08c18-113">Remarks</span></span>

<span data-ttu-id="08c18-114">使用下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="08c18-114">Use one of the following values.</span></span>



| <span data-ttu-id="08c18-115">值</span><span class="sxs-lookup"><span data-stu-id="08c18-115">Value</span></span> | <span data-ttu-id="08c18-116">描述</span><span class="sxs-lookup"><span data-stu-id="08c18-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="08c18-117">0</span><span class="sxs-lookup"><span data-stu-id="08c18-117">0</span></span>     | <span data-ttu-id="08c18-118">漸進式</span><span class="sxs-lookup"><span data-stu-id="08c18-118">Progressive</span></span> |
| <span data-ttu-id="08c18-119">2</span><span class="sxs-lookup"><span data-stu-id="08c18-119">2</span></span>     | <span data-ttu-id="08c18-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="08c18-120">Interlaced</span></span>  |



 

<span data-ttu-id="08c18-121">如果未設定此屬性，則 DSP 會使用輸入媒體類型來判斷影片是否為交錯式。</span><span class="sxs-lookup"><span data-stu-id="08c18-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="08c18-122">您可以設定這個屬性來覆寫媒體類型設定。</span><span class="sxs-lookup"><span data-stu-id="08c18-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="08c18-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="08c18-123">Requirements</span></span>



| <span data-ttu-id="08c18-124">需求</span><span class="sxs-lookup"><span data-stu-id="08c18-124">Requirement</span></span> | <span data-ttu-id="08c18-125">值</span><span class="sxs-lookup"><span data-stu-id="08c18-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08c18-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08c18-126">Minimum supported client</span></span><br/> | <span data-ttu-id="08c18-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08c18-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="08c18-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08c18-128">Minimum supported server</span></span><br/> | <span data-ttu-id="08c18-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08c18-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08c18-130">標頭</span><span class="sxs-lookup"><span data-stu-id="08c18-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="08c18-131"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="08c18-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08c18-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08c18-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c18-133">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="08c18-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

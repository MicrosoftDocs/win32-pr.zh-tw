---
description: 指定編碼演算法的複雜度。
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: 'MFPKEY_ENCCOMPLEXITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f50e7966a05affe8ae75869b670cf75f088b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848814"
---
# <a name="mfpkey_enccomplexity-property"></a><span data-ttu-id="1296e-103">MFPKEY \_ ENCCOMPLEXITY 屬性</span><span class="sxs-lookup"><span data-stu-id="1296e-103">MFPKEY\_ENCCOMPLEXITY Property</span></span>

<span data-ttu-id="1296e-104">指定編碼演算法的複雜度。</span><span class="sxs-lookup"><span data-stu-id="1296e-104">Specifies the complexity of the encoding algorithm.</span></span> <span data-ttu-id="1296e-105">值是介於0與100之間的整數，其中0指定最不復雜的演算法，而100則指定最複雜的演算法。</span><span class="sxs-lookup"><span data-stu-id="1296e-105">The value is an integer between 0 and 100, where 0 specifies the least complex algorithm, and 100 specifies the most complex algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1296e-106">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="1296e-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="1296e-107">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="1296e-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1296e-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="1296e-108">Data Type</span></span>

<span data-ttu-id="1296e-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="1296e-109">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="1296e-110">預設值</span><span class="sxs-lookup"><span data-stu-id="1296e-110">Default Value</span></span>

<span data-ttu-id="1296e-111">100 Windows Media 音訊10和 Windows Media 音訊10專業版</span><span class="sxs-lookup"><span data-stu-id="1296e-111">100 for Windows Media Audio 10 and Windows Media Audio 10 Professional</span></span>

<span data-ttu-id="1296e-112">100適用于 Windows Vista 版本的 Windows Media 音訊10無損</span><span class="sxs-lookup"><span data-stu-id="1296e-112">100 for the Windows Vista release of Windows Media Audio 10 Lossless</span></span>

<span data-ttu-id="1296e-113">0適用于 Windows 7 release Windows Media 音訊10無損</span><span class="sxs-lookup"><span data-stu-id="1296e-113">0 for the Windows 7 release Windows Media Audio 10 Lossless</span></span>

## <a name="remarks"></a><span data-ttu-id="1296e-114">備註</span><span class="sxs-lookup"><span data-stu-id="1296e-114">Remarks</span></span>

<span data-ttu-id="1296e-115">如果 [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) 屬性的值為 **VARIANT \_ TRUE**，編碼器會根據此屬性的值來調整其演算法的複雜度。</span><span class="sxs-lookup"><span data-stu-id="1296e-115">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_TRUE**, the encoder adjusts the complexity of its algorithm according to the value of this property.</span></span>

<span data-ttu-id="1296e-116">針對 Windows Media 音訊10編碼器和 Windows Media 音訊10專業版編碼器，如果此屬性的值為100，則編碼器會對 CPU 產生高需求，並產生最高品質的輸出。</span><span class="sxs-lookup"><span data-stu-id="1296e-116">For the Windows Media Audio 10 encoder and the Windows Media Audio 10 Professional encoder, if the value of this property is 100, the encoder places a high demand on the CPU and produces the highest quality output.</span></span> <span data-ttu-id="1296e-117">當此屬性的值減少時，CPU 的需求會減少，但輸出品質也會減少。</span><span class="sxs-lookup"><span data-stu-id="1296e-117">As the value of this property decreases, the demand on the CPU decreases, but the quality of the output also decreases.</span></span>

<span data-ttu-id="1296e-118">針對 Windows Media 音訊10個無失真編碼器，如果此屬性的值為0，則編碼器會對 CPU 造成較低的需求。</span><span class="sxs-lookup"><span data-stu-id="1296e-118">For the Windows Media Audio 10 Lossless encoder, if the value of this property is 0, the encoder places a low demand on the CPU.</span></span> <span data-ttu-id="1296e-119">當此屬性的值增加時，CPU 的需求會增加，而且編碼器輸出的大小會稍微減少。</span><span class="sxs-lookup"><span data-stu-id="1296e-119">As the value of this property increases, the demand on the CPU increases, and the size of the encoder output decreases slightly.</span></span> <span data-ttu-id="1296e-120">無論這個屬性的值為何，輸出都不會失真。</span><span class="sxs-lookup"><span data-stu-id="1296e-120">The output is lossless regardless of the value of this property.</span></span>

<span data-ttu-id="1296e-121">如果您將此屬性保留為 **變數 \_ FALSE** 的預設值，則編碼器會使用它的預設演算法。</span><span class="sxs-lookup"><span data-stu-id="1296e-121">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder uses its default algorithm.</span></span> <span data-ttu-id="1296e-122">預設演算法取決於您所使用的編碼器，以及正在執行的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="1296e-122">The default algorithm depends on which encoder you are using and which version of Windows is running.</span></span> <span data-ttu-id="1296e-123">下表描述不同組合的預設行為。</span><span class="sxs-lookup"><span data-stu-id="1296e-123">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="1296e-124">作業系統</span><span class="sxs-lookup"><span data-stu-id="1296e-124">Operating system</span></span> | <span data-ttu-id="1296e-125">預設行為</span><span class="sxs-lookup"><span data-stu-id="1296e-125">Default behavior</span></span>                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1296e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1296e-126">Windows Vista</span></span>    | <span data-ttu-id="1296e-127">Windows Media 音訊10、Windows Media 音訊10專業版和 Windows Media 音訊10個無失真編碼器預設都會使用最複雜的演算法。</span><span class="sxs-lookup"><span data-stu-id="1296e-127">The Windows Media Audio 10, Windows Media Audio 10 Professional, and Windows Media Audio 10 Lossless encoders all use the most complex algorithm by default.</span></span>                                                    |
| <span data-ttu-id="1296e-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1296e-128">Windows 7</span></span>        | <span data-ttu-id="1296e-129">Windows Media 音訊10和 Windows Media 音訊10專業版編碼器預設會使用最複雜的演算法。</span><span class="sxs-lookup"><span data-stu-id="1296e-129">The Windows Media Audio 10 and Windows Media Audio 10 Professional encoders use the most complex algorithm by default.</span></span> <span data-ttu-id="1296e-130">Windows Media 音訊10個無失真編碼器預設會使用最不復雜的演算法。</span><span class="sxs-lookup"><span data-stu-id="1296e-130">The Windows Media Audio 10 Lossless encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="1296e-131">如果 [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) 屬性的值為 **VARIANT \_ FALSE**，則編碼器會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1296e-131">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_FALSE**, the encoder ignores this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1296e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="1296e-132">Requirements</span></span>



| <span data-ttu-id="1296e-133">需求</span><span class="sxs-lookup"><span data-stu-id="1296e-133">Requirement</span></span> | <span data-ttu-id="1296e-134">值</span><span class="sxs-lookup"><span data-stu-id="1296e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1296e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1296e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1296e-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1296e-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1296e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1296e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1296e-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1296e-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1296e-139">標頭</span><span class="sxs-lookup"><span data-stu-id="1296e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1296e-140"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1296e-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1296e-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1296e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1296e-142">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="1296e-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

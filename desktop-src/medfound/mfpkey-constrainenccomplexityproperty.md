---
description: 指定是否限制音訊編碼演算法的複雜度。
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: 'MFPKEY_CONSTRAINENCOMPLEXITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997519"
---
# <a name="mfpkey_constrainencomplexity-property"></a><span data-ttu-id="a08b5-103">MFPKEY \_ CONSTRAINENCOMPLEXITY 屬性</span><span class="sxs-lookup"><span data-stu-id="a08b5-103">MFPKEY\_CONSTRAINENCOMPLEXITY Property</span></span>

<span data-ttu-id="a08b5-104">指定是否限制音訊編碼演算法的複雜度。</span><span class="sxs-lookup"><span data-stu-id="a08b5-104">Specifies whether the complexity of the audio encoding algorithm is constrained.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a08b5-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="a08b5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a08b5-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="a08b5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="a08b5-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="a08b5-107">Data Type</span></span>

<span data-ttu-id="a08b5-108">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="a08b5-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="a08b5-109">預設值</span><span class="sxs-lookup"><span data-stu-id="a08b5-109">Default Value</span></span>

<span data-ttu-id="a08b5-110">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="a08b5-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="a08b5-111">備註</span><span class="sxs-lookup"><span data-stu-id="a08b5-111">Remarks</span></span>

<span data-ttu-id="a08b5-112">如果您將此屬性保留為預設值 [ **VARIANT \_ FALSE**]，則音訊編碼器會使用它的預設演算法。</span><span class="sxs-lookup"><span data-stu-id="a08b5-112">If you leave this property at its default value of **VARIANT\_FALSE**, the audio encoder uses its default algorithm.</span></span> <span data-ttu-id="a08b5-113">預設演算法取決於輸出類型以及正在執行的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="a08b5-113">The default algorithm depends on the output type and which version of Windows is running.</span></span> <span data-ttu-id="a08b5-114">下表描述不同組合的預設行為。</span><span class="sxs-lookup"><span data-stu-id="a08b5-114">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="a08b5-115">作業系統</span><span class="sxs-lookup"><span data-stu-id="a08b5-115">Operating system</span></span> | <span data-ttu-id="a08b5-116">預設行為</span><span class="sxs-lookup"><span data-stu-id="a08b5-116">Default behavior</span></span>                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a08b5-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a08b5-117">Windows Vista</span></span>    | <span data-ttu-id="a08b5-118">針對所有輸出類型，音訊編碼器預設會使用最複雜的演算法。</span><span class="sxs-lookup"><span data-stu-id="a08b5-118">For all output types, the audio encoder uses the most complex algorithm by default.</span></span>                                                                                                                 |
| <span data-ttu-id="a08b5-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a08b5-119">Windows 7</span></span>        | <span data-ttu-id="a08b5-120">針對標準和專業輸出類型，音訊編碼器預設會使用最複雜的演算法。</span><span class="sxs-lookup"><span data-stu-id="a08b5-120">For Standard and Professional output types, the audio encoder uses the most complex algorithm by default.</span></span> <span data-ttu-id="a08b5-121">針對無損輸出類型，音訊編碼器預設會使用最不復雜的演算法。</span><span class="sxs-lookup"><span data-stu-id="a08b5-121">For Lossless output types, the audio encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="a08b5-122">如果您將此屬性設定為 **VARIANT \_ TRUE**，您也必須藉由設定 [**MFPKEY \_ ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) 屬性來指定複雜度值。</span><span class="sxs-lookup"><span data-stu-id="a08b5-122">If you set this property to **VARIANT\_TRUE**, you must also specify a complexity value by setting the [**MFPKEY\_ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a08b5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a08b5-123">Requirements</span></span>



| <span data-ttu-id="a08b5-124">需求</span><span class="sxs-lookup"><span data-stu-id="a08b5-124">Requirement</span></span> | <span data-ttu-id="a08b5-125">值</span><span class="sxs-lookup"><span data-stu-id="a08b5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a08b5-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a08b5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a08b5-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a08b5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a08b5-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a08b5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a08b5-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a08b5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a08b5-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a08b5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a08b5-131"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a08b5-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a08b5-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a08b5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08b5-133">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="a08b5-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

---
description: 指定核心編碼器是否使用 &\# 0034;加上&\# 0034; 功能。
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: 'MFPKEY_ENHANCED_WMA 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999734"
---
# <a name="mfpkey_enhanced_wma-property"></a><span data-ttu-id="cadfb-103">MFPKEY \_ 增強型 \_ WMA 屬性</span><span class="sxs-lookup"><span data-stu-id="cadfb-103">MFPKEY\_ENHANCED\_WMA Property</span></span>

<span data-ttu-id="cadfb-104">指定核心編碼器是否使用「加號」功能。</span><span class="sxs-lookup"><span data-stu-id="cadfb-104">Specifies whether the core encoder uses the "Plus" feature.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cadfb-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="cadfb-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cadfb-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="cadfb-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="cadfb-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="cadfb-107">Data Type</span></span>

<span data-ttu-id="cadfb-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="cadfb-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="cadfb-109">預設值</span><span class="sxs-lookup"><span data-stu-id="cadfb-109">Default Value</span></span>

<span data-ttu-id="cadfb-110">0</span><span class="sxs-lookup"><span data-stu-id="cadfb-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="cadfb-111">備註</span><span class="sxs-lookup"><span data-stu-id="cadfb-111">Remarks</span></span>

<span data-ttu-id="cadfb-112">這個屬性僅適用于 Windows Media 音訊無損。</span><span class="sxs-lookup"><span data-stu-id="cadfb-112">This property is available only for Windows Media Audio Lossless.</span></span>

<span data-ttu-id="cadfb-113">如果您將此屬性保留為預設值0，或將它設定為1，核心編碼器會決定是否應該使用 "Plus" 部分。</span><span class="sxs-lookup"><span data-stu-id="cadfb-113">If you leave this property at its default value of 0, or if you set it to 1, the core encoder decides whether the "Plus" portion should be used.</span></span> <span data-ttu-id="cadfb-114">如果您將此屬性設定為2，則核心編碼器不會使用 "Plus" 功能。</span><span class="sxs-lookup"><span data-stu-id="cadfb-114">If you set this property to 2, the core encoder does not use the "Plus" feature.</span></span>

<span data-ttu-id="cadfb-115">這個屬性會改變列舉的媒體類型，因此，如果您設定它，就必須在設定輸出類型之前先這麼做。</span><span class="sxs-lookup"><span data-stu-id="cadfb-115">This property alters the enumerated media types, so if you set it, you must do so before you set the output type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cadfb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cadfb-116">Requirements</span></span>



| <span data-ttu-id="cadfb-117">需求</span><span class="sxs-lookup"><span data-stu-id="cadfb-117">Requirement</span></span> | <span data-ttu-id="cadfb-118">值</span><span class="sxs-lookup"><span data-stu-id="cadfb-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cadfb-119">用戶端</span><span class="sxs-lookup"><span data-stu-id="cadfb-119">Client</span></span><br/> | <span data-ttu-id="cadfb-120">Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="cadfb-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="cadfb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="cadfb-121">Header</span></span><br/> | <dl> <span data-ttu-id="cadfb-122"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="cadfb-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cadfb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cadfb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cadfb-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="cadfb-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

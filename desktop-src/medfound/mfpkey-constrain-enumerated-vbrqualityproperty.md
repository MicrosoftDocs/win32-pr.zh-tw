---
description: 指定是否將編碼器所列舉的模式 limeted 至符合 MFPKEY \_ 所需 VBRQUALITY 所指定之品質需求的模式 \_ 。
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: 'MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991035"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a><span data-ttu-id="57ad8-103">MFPKEY \_ 限制 \_ 列舉的 \_ VBRQUALITY 屬性</span><span class="sxs-lookup"><span data-stu-id="57ad8-103">MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="57ad8-104">指定是否將編碼器所列舉的模式 limeted 至符合 [**MFPKEY \_ 所需 \_ VBRQUALITY 所**](mfpkey-desired-vbrqualityproperty.md)指定之品質需求的模式。</span><span class="sxs-lookup"><span data-stu-id="57ad8-104">Specifies whether modes enumerated by the encoder are limeted to those that meet a quality requirement given by [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="57ad8-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="57ad8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="57ad8-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="57ad8-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="57ad8-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="57ad8-107">Data Type</span></span>

<span data-ttu-id="57ad8-108">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="57ad8-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="57ad8-109">預設值</span><span class="sxs-lookup"><span data-stu-id="57ad8-109">Default Value</span></span>

<span data-ttu-id="57ad8-110">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="57ad8-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="57ad8-111">備註</span><span class="sxs-lookup"><span data-stu-id="57ad8-111">Remarks</span></span>

<span data-ttu-id="57ad8-112">若要列舉符合特定品質需求的 VBR 模式，請設定下列編碼器屬性。</span><span class="sxs-lookup"><span data-stu-id="57ad8-112">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="57ad8-113">將 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="57ad8-113">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="57ad8-114">Set **MFPKEY \_ 將 \_ 列舉的 \_ VBRQUALITY 限制** 為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="57ad8-114">Set **MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY** to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="57ad8-115">將 [**MFPKEY \_ 所需的 \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) 設定為所需的品質。</span><span class="sxs-lookup"><span data-stu-id="57ad8-115">Set [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) to the desired quality.</span></span> <span data-ttu-id="57ad8-116">若為不失真模式，請將所需的品質設定為100。</span><span class="sxs-lookup"><span data-stu-id="57ad8-116">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ad8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="57ad8-117">Requirements</span></span>



| <span data-ttu-id="57ad8-118">需求</span><span class="sxs-lookup"><span data-stu-id="57ad8-118">Requirement</span></span> | <span data-ttu-id="57ad8-119">值</span><span class="sxs-lookup"><span data-stu-id="57ad8-119">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57ad8-120">用戶端</span><span class="sxs-lookup"><span data-stu-id="57ad8-120">Client</span></span><br/> | <span data-ttu-id="57ad8-121">Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="57ad8-121">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="57ad8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="57ad8-122">Header</span></span><br/> | <dl> <span data-ttu-id="57ad8-123"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="57ad8-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57ad8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57ad8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ad8-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="57ad8-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

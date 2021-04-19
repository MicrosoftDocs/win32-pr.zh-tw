---
description: 指定編碼器是否應使用每個畫面格的樣本數所提供的慣用框架大小。
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: 'MFPKEY_REQUESTING_A_FRAMESIZE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979617"
---
# <a name="mfpkey_requesting_a_framesize-property"></a><span data-ttu-id="46f1b-103">MFPKEY \_ 要求 \_ \_ FRAMESIZE 屬性</span><span class="sxs-lookup"><span data-stu-id="46f1b-103">MFPKEY\_REQUESTING\_A\_FRAMESIZE Property</span></span>

<span data-ttu-id="46f1b-104">指定編碼器是否應使用每個畫面格的樣本數所提供的慣用框架大小。</span><span class="sxs-lookup"><span data-stu-id="46f1b-104">Specifies whether the encoder should use a preferred frame size given in number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="46f1b-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="46f1b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="46f1b-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="46f1b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="46f1b-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="46f1b-107">Data Type</span></span>

<span data-ttu-id="46f1b-108">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="46f1b-108">**VT\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="46f1b-109">備註</span><span class="sxs-lookup"><span data-stu-id="46f1b-109">Remarks</span></span>

<span data-ttu-id="46f1b-110">若要指定慣用的框架大小，請設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="46f1b-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="46f1b-111">將 **\_ 要求 \_ \_ FRAMESIZE 的 MFPKEY** 設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="46f1b-111">Set **MFPKEY\_REQUESTING\_A\_FRAMESIZE** to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="46f1b-112">將 [**MFPKEY \_ 偏好 \_ FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) 設定為每個畫面格所需的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="46f1b-112">Set [**MFPKEY\_PREFERRED\_FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="46f1b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="46f1b-113">Requirements</span></span>



| <span data-ttu-id="46f1b-114">需求</span><span class="sxs-lookup"><span data-stu-id="46f1b-114">Requirement</span></span> | <span data-ttu-id="46f1b-115">值</span><span class="sxs-lookup"><span data-stu-id="46f1b-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46f1b-116">用戶端</span><span class="sxs-lookup"><span data-stu-id="46f1b-116">Client</span></span><br/> | <span data-ttu-id="46f1b-117">Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="46f1b-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="46f1b-118">標頭</span><span class="sxs-lookup"><span data-stu-id="46f1b-118">Header</span></span><br/> | <dl> <span data-ttu-id="46f1b-119"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="46f1b-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46f1b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46f1b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f1b-121">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="46f1b-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

---
description: 指定每個框架慣用的樣本數目。
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: 'MFPKEY_PREFERRED_FRAMESIZE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000990"
---
# <a name="mfpkey_preferred_framesize-property"></a><span data-ttu-id="2cb52-103">MFPKEY \_ 慣用 \_ FRAMESIZE 屬性</span><span class="sxs-lookup"><span data-stu-id="2cb52-103">MFPKEY\_PREFERRED\_FRAMESIZE Property</span></span>

<span data-ttu-id="2cb52-104">指定每個框架慣用的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="2cb52-104">Specifies the preferred number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2cb52-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="2cb52-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2cb52-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="2cb52-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2cb52-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="2cb52-107">Data Type</span></span>

<span data-ttu-id="2cb52-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="2cb52-108">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="2cb52-109">備註</span><span class="sxs-lookup"><span data-stu-id="2cb52-109">Remarks</span></span>

<span data-ttu-id="2cb52-110">若要指定慣用的框架大小，請設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="2cb52-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="2cb52-111">將 [**\_ 要求 \_ \_ FRAMESIZE 的 MFPKEY**](mfpkey-requesting-a-framesizeproperty.md) 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="2cb52-111">Set [**MFPKEY\_REQUESTING\_A\_FRAMESIZE**](mfpkey-requesting-a-framesizeproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="2cb52-112">將 **MFPKEY \_ 偏好 \_ FRAMESIZE** 設定為每個畫面格所需的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="2cb52-112">Set **MFPKEY\_PREFERRED\_FRAMESIZE** to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cb52-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cb52-113">Requirements</span></span>



| <span data-ttu-id="2cb52-114">需求</span><span class="sxs-lookup"><span data-stu-id="2cb52-114">Requirement</span></span> | <span data-ttu-id="2cb52-115">值</span><span class="sxs-lookup"><span data-stu-id="2cb52-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb52-116">用戶端</span><span class="sxs-lookup"><span data-stu-id="2cb52-116">Client</span></span><br/> | <span data-ttu-id="2cb52-117">Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="2cb52-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="2cb52-118">標頭</span><span class="sxs-lookup"><span data-stu-id="2cb52-118">Header</span></span><br/> | <dl> <span data-ttu-id="2cb52-119"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2cb52-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cb52-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cb52-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb52-121">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="2cb52-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

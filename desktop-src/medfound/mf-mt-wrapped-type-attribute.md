---
description: 包含已經換成另一種媒體類型的媒體類型。
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: 'MF_MT_WRAPPED_TYPE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad09c69f7b99c2c376a207270cadb034e735546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386024"
---
# <a name="mf_mt_wrapped_type-attribute"></a><span data-ttu-id="fd0ad-103">MF \_ MT \_ 包裝 \_ 型別屬性</span><span class="sxs-lookup"><span data-stu-id="fd0ad-103">MF\_MT\_WRAPPED\_TYPE attribute</span></span>

<span data-ttu-id="fd0ad-104">包含已經換成另一種媒體類型的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="fd0ad-104">Contains a media type that has been wrapped in another media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd0ad-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="fd0ad-105">Data type</span></span>

<span data-ttu-id="fd0ad-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="fd0ad-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="fd0ad-107">備註</span><span class="sxs-lookup"><span data-stu-id="fd0ad-107">Remarks</span></span>

<span data-ttu-id="fd0ad-108">這個屬性是在 [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) 函式中使用，該函式會將媒體類型包裝在另一個媒體類型內。</span><span class="sxs-lookup"><span data-stu-id="fd0ad-108">This attribute is used in the [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function, which wraps a media type inside another media type.</span></span>

<span data-ttu-id="fd0ad-109">[**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)函式會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="fd0ad-109">The [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function does the following:</span></span>

1.  <span data-ttu-id="fd0ad-110">將原始媒體類型轉換成二進位陣列。</span><span class="sxs-lookup"><span data-stu-id="fd0ad-110">Converts the original media type into a binary array.</span></span>
2.  <span data-ttu-id="fd0ad-111">在新的媒體類型上設定 **MF \_ MT \_ 包裝 \_ 型** 別屬性。</span><span class="sxs-lookup"><span data-stu-id="fd0ad-111">Sets the **MF\_MT\_WRAPPED\_TYPE** attribute on the new media type.</span></span> <span data-ttu-id="fd0ad-112">屬性的值是二進位陣列。</span><span class="sxs-lookup"><span data-stu-id="fd0ad-112">The value of the attribute is the binary array.</span></span>

<span data-ttu-id="fd0ad-113">應用程式通常不會直接使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="fd0ad-113">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="fd0ad-114">若要解除包裝原始媒體類型，請呼叫 [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype)。</span><span class="sxs-lookup"><span data-stu-id="fd0ad-114">To unwrap the original media type, call [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span></span>

<span data-ttu-id="fd0ad-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="fd0ad-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd0ad-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd0ad-116">Requirements</span></span>



| <span data-ttu-id="fd0ad-117">需求</span><span class="sxs-lookup"><span data-stu-id="fd0ad-117">Requirement</span></span> | <span data-ttu-id="fd0ad-118">值</span><span class="sxs-lookup"><span data-stu-id="fd0ad-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0ad-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd0ad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd0ad-120">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd0ad-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="fd0ad-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd0ad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd0ad-122">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd0ad-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fd0ad-123">標頭</span><span class="sxs-lookup"><span data-stu-id="fd0ad-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd0ad-124"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd0ad-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd0ad-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd0ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0ad-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="fd0ad-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd0ad-127">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="fd0ad-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="fd0ad-128">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="fd0ad-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="fd0ad-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="fd0ad-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="fd0ad-130">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="fd0ad-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 





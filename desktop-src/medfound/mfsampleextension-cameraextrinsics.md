---
description: 包含範例的相機 extrinsics。
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: 'MFSampleExtension_CameraExtrinsics 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3340f1ab84061fa00e12fa65960f1b2902690816
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976790"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a><span data-ttu-id="33758-103">MFSampleExtension \_ CameraExtrinsics 屬性</span><span class="sxs-lookup"><span data-stu-id="33758-103">MFSampleExtension\_CameraExtrinsics attribute</span></span>

<span data-ttu-id="33758-104">包含範例的相機 extrinsics。</span><span class="sxs-lookup"><span data-stu-id="33758-104">Contains the camera extrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="33758-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="33758-105">Data type</span></span>

<span data-ttu-id="33758-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="33758-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="33758-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="33758-107">Get/set</span></span>

<span data-ttu-id="33758-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。</span><span class="sxs-lookup"><span data-stu-id="33758-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="33758-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。</span><span class="sxs-lookup"><span data-stu-id="33758-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="33758-110">適用於</span><span class="sxs-lookup"><span data-stu-id="33758-110">Applies to</span></span>

[<span data-ttu-id="33758-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="33758-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="33758-112">備註</span><span class="sxs-lookup"><span data-stu-id="33758-112">Remarks</span></span>

<span data-ttu-id="33758-113">屬性的值是 [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics)。</span><span class="sxs-lookup"><span data-stu-id="33758-113">The value of the attribute is a [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span></span>

<span data-ttu-id="33758-114">這個屬性是選擇性的，可支援未校正的相機。</span><span class="sxs-lookup"><span data-stu-id="33758-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="33758-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="33758-115">Requirements</span></span>



| <span data-ttu-id="33758-116">需求</span><span class="sxs-lookup"><span data-stu-id="33758-116">Requirement</span></span> | <span data-ttu-id="33758-117">值</span><span class="sxs-lookup"><span data-stu-id="33758-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="33758-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33758-118">Minimum supported client</span></span><br/> | <span data-ttu-id="33758-119">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33758-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33758-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33758-120">Minimum supported server</span></span><br/> | <span data-ttu-id="33758-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33758-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="33758-122">標頭</span><span class="sxs-lookup"><span data-stu-id="33758-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="33758-123"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="33758-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33758-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33758-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33758-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="33758-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





---
description: 強制編碼器將下一個畫面格編碼為主要畫面格。
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: 'CODECAPI_AVEncVideoForceKeyFrame 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973198"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a><span data-ttu-id="a9492-103">CODECAPI \_ AVEncVideoForceKeyFrame 屬性</span><span class="sxs-lookup"><span data-stu-id="a9492-103">CODECAPI\_AVEncVideoForceKeyFrame property</span></span>

<span data-ttu-id="a9492-104">強制編碼器將下一個畫面格編碼為主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="a9492-104">Forces the encoder to code the next frame as a key frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="a9492-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a9492-105">Data type</span></span>

<span data-ttu-id="a9492-106">**ULONG** (VT \_ UI4) </span><span class="sxs-lookup"><span data-stu-id="a9492-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a9492-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="a9492-107">Property GUID</span></span>

<span data-ttu-id="a9492-108">**CODECAPI \_ AVEncVideoForceKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="a9492-108">**CODECAPI\_AVEncVideoForceKeyFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="a9492-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="a9492-109">Property value</span></span>

<span data-ttu-id="a9492-110">如果此值為非零值，則編碼器會將下一個畫面格編碼為主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="a9492-110">If the value is nonzero, the encoder will code the next frame as a key frame.</span></span> <span data-ttu-id="a9492-111">如果值為零，則編碼器會選取是否要將下一個框架編碼為主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="a9492-111">If the value is zero, the encoder selects whether to encode the next frame as a key frame.</span></span>

<span data-ttu-id="a9492-112">這個屬性會套用至編碼器接收為輸入的下一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="a9492-112">This property applies to the next frame that the encoder receives as input.</span></span> <span data-ttu-id="a9492-113">針對媒體基礎轉換 (MFT) ，這是傳遞至 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 方法的下一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="a9492-113">For a Media Foundation transform (MFT), this is the next frame that is passed to the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method.</span></span> <span data-ttu-id="a9492-114">在下一個畫面格之後，此設定會重設為零。</span><span class="sxs-lookup"><span data-stu-id="a9492-114">The setting resets to zero after the next frame.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9492-115">備註</span><span class="sxs-lookup"><span data-stu-id="a9492-115">Remarks</span></span>

<span data-ttu-id="a9492-116">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="a9492-116">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9492-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9492-117">Requirements</span></span>



| <span data-ttu-id="a9492-118">需求</span><span class="sxs-lookup"><span data-stu-id="a9492-118">Requirement</span></span> | <span data-ttu-id="a9492-119">值</span><span class="sxs-lookup"><span data-stu-id="a9492-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9492-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9492-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a9492-121">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9492-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="a9492-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9492-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a9492-123">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9492-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a9492-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a9492-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9492-125"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9492-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9492-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9492-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9492-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="a9492-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a9492-128">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a9492-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 


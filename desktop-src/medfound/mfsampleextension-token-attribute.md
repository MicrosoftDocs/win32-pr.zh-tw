---
description: 包含提供給 IMFMediaStream：： RequestSample 方法之權杖的指標。
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: 'MFSampleExtension_Token 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978844"
---
# <a name="mfsampleextension_token-attribute"></a><span data-ttu-id="e34b7-103">MFSampleExtension \_ Token 屬性</span><span class="sxs-lookup"><span data-stu-id="e34b7-103">MFSampleExtension\_Token attribute</span></span>

<span data-ttu-id="e34b7-104">包含提供給 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 方法之權杖的指標。</span><span class="sxs-lookup"><span data-stu-id="e34b7-104">Contains a pointer to the token that was provided to the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

## <a name="data-type"></a><span data-ttu-id="e34b7-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e34b7-105">Data type</span></span>

<span data-ttu-id="e34b7-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="e34b7-106">\**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="e34b7-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="e34b7-107">Get/set</span></span>

<span data-ttu-id="e34b7-108">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="e34b7-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="e34b7-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="e34b7-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e34b7-110">適用於</span><span class="sxs-lookup"><span data-stu-id="e34b7-110">Applies to</span></span>

[<span data-ttu-id="e34b7-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="e34b7-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="e34b7-112">備註</span><span class="sxs-lookup"><span data-stu-id="e34b7-112">Remarks</span></span>

<span data-ttu-id="e34b7-113">這個屬性會套用至媒體範例。</span><span class="sxs-lookup"><span data-stu-id="e34b7-113">This attribute applies to media samples.</span></span> <span data-ttu-id="e34b7-114">屬性的值是傳遞給 [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)方法之 *PToken* 參數的 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="e34b7-114">The value of the attribute is the **IUnknown** pointer that is passed to the *pToken* parameter of the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span> <span data-ttu-id="e34b7-115">呼叫端會使用這個屬性來追蹤要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="e34b7-115">The caller uses this attribute to track the status of the request.</span></span>

<span data-ttu-id="e34b7-116">如果您要撰寫自訂媒體來源，則在媒體串流傳遞範例以回應 [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 方法時，請在範例上設定此屬性，除非 *pToken* 的值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e34b7-116">If you are writing a custom media source, set this attribute on the sample when the media stream delivers a sample in response to the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method, unless the value of *pToken* is **NULL**.</span></span>

<span data-ttu-id="e34b7-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e34b7-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e34b7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e34b7-118">Requirements</span></span>



| <span data-ttu-id="e34b7-119">需求</span><span class="sxs-lookup"><span data-stu-id="e34b7-119">Requirement</span></span> | <span data-ttu-id="e34b7-120">值</span><span class="sxs-lookup"><span data-stu-id="e34b7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e34b7-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e34b7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e34b7-122">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e34b7-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e34b7-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e34b7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e34b7-124">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e34b7-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e34b7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e34b7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e34b7-126"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e34b7-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e34b7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e34b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e34b7-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e34b7-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e34b7-129">範例屬性</span><span class="sxs-lookup"><span data-stu-id="e34b7-129">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="e34b7-130">媒體範例</span><span class="sxs-lookup"><span data-stu-id="e34b7-130">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 





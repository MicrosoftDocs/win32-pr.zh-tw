---
description: 指定 ASF 媒體接收器是否自動調整位元速率。
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: 'MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106998948"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a><span data-ttu-id="c5947-103">MFPKEY \_ ASFMEDIASINK \_ AUTOADJUST \_ 位元速率屬性</span><span class="sxs-lookup"><span data-stu-id="c5947-103">MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE property</span></span>

<span data-ttu-id="c5947-104">指定 ASF 媒體接收器是否自動調整位元速率。</span><span class="sxs-lookup"><span data-stu-id="c5947-104">Specifies whether the ASF media sink automatically adjusts the bit rate.</span></span>



<span data-ttu-id="c5947-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c5947-105">Data type</span></span>

<span data-ttu-id="c5947-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="c5947-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c5947-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="c5947-107">PROPVARIANT member</span></span>

<span data-ttu-id="c5947-108">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c5947-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="c5947-109">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="c5947-109">VT\_BOOL</span></span>

<span data-ttu-id="c5947-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="c5947-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c5947-111">備註</span><span class="sxs-lookup"><span data-stu-id="c5947-111">Remarks</span></span>

<span data-ttu-id="c5947-112">如果這個屬性的值為 VARIANT \_ ，則 asf 媒體接收器會自動調整 asf 內容的位元速率，以回應多工處理的資料流程特性。</span><span class="sxs-lookup"><span data-stu-id="c5947-112">If the value of this property is VARIANT\_TRUE, the ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span>

<span data-ttu-id="c5947-113">這個屬性會影響當資料流程溢出接收的 "有漏洞 bucket" 參數時，ASF 媒體接收器的行為：</span><span class="sxs-lookup"><span data-stu-id="c5947-113">This property affects how the ASF media sink behaves when a stream overflows the sink's "leaky bucket" parameters:</span></span>



| <span data-ttu-id="c5947-114">值</span><span class="sxs-lookup"><span data-stu-id="c5947-114">Value</span></span>              | <span data-ttu-id="c5947-115">行為</span><span class="sxs-lookup"><span data-stu-id="c5947-115">Behavior</span></span>                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5947-116">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="c5947-116">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="c5947-117">ASF 媒體接收器會自動調整 ASF 內容的位元速率，以回應多工處理的資料流程特性。</span><span class="sxs-lookup"><span data-stu-id="c5947-117">The ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span> |
| <span data-ttu-id="c5947-118">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="c5947-118">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="c5947-119">ASF 媒體接收器會使用應用程式所提供的資料流程位元速率值。</span><span class="sxs-lookup"><span data-stu-id="c5947-119">The ASF media sink uses the stream bit rate value provided by the application.</span></span>                                                                |



 

<span data-ttu-id="c5947-120">預設值為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c5947-120">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="c5947-121">當您設定 ASF 媒體接收時，請設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="c5947-121">Set this property when you configure the ASF media sink.</span></span> <span data-ttu-id="c5947-122">使用方式取決於您所呼叫用來建立 ASF 媒體接收器的函式：</span><span class="sxs-lookup"><span data-stu-id="c5947-122">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="c5947-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)：查詢 **IPropertyStore** 介面的已取出 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)指標。</span><span class="sxs-lookup"><span data-stu-id="c5947-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="c5947-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)：在 *pContentInfo* 參數中指定的 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)指標上呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) 。</span><span class="sxs-lookup"><span data-stu-id="c5947-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

<span data-ttu-id="c5947-125">將此屬性設定為 VARIANT \_ TRUE 會導致 asf 媒體接收器在 asf 多工器上設定 MFASF 多工器 **\_ \_ AUTOADJUST \_ 位元速率** 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5947-125">Setting this property to VARIANT\_TRUE causes the ASF media sink to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag on the ASF multiplexer.</span></span> <span data-ttu-id="c5947-126">請參閱 [**IMFASFMultiplexer：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags)。</span><span class="sxs-lookup"><span data-stu-id="c5947-126">See [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span></span>

<span data-ttu-id="c5947-127">如需有關有漏洞 bucket 概念的詳細資訊，請參閱 Windows Media Format SDK 檔中的「有漏洞 Bucket 緩衝區模型」主題。</span><span class="sxs-lookup"><span data-stu-id="c5947-127">For more information about the leaky bucket concept, see the topic "The Leaky Bucket Buffer Model" in the Windows Media Format SDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5947-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5947-128">Requirements</span></span>



| <span data-ttu-id="c5947-129">需求</span><span class="sxs-lookup"><span data-stu-id="c5947-129">Requirement</span></span> | <span data-ttu-id="c5947-130">值</span><span class="sxs-lookup"><span data-stu-id="c5947-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5947-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5947-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c5947-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5947-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c5947-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5947-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c5947-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5947-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c5947-135">標頭</span><span class="sxs-lookup"><span data-stu-id="c5947-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5947-136"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5947-136"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5947-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5947-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5947-138">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="c5947-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c5947-139">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="c5947-139">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[<span data-ttu-id="c5947-140">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="c5947-140">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 





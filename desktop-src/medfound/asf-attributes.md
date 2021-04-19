---
description: ASF 屬性
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: ASF 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973597"
---
# <a name="asf-attributes"></a><span data-ttu-id="0bd72-103">ASF 屬性</span><span class="sxs-lookup"><span data-stu-id="0bd72-103">ASF Attributes</span></span>

### <a name="profile-attributes"></a><span data-ttu-id="0bd72-104">配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="0bd72-104">Profile Attributes</span></span>

<span data-ttu-id="0bd72-105">下列屬性適用于 ASF 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0bd72-105">The following attributes apply to ASF profiles.</span></span>



| <span data-ttu-id="0bd72-106">屬性</span><span class="sxs-lookup"><span data-stu-id="0bd72-106">Attribute</span></span>                                                                      | <span data-ttu-id="0bd72-107">描述</span><span class="sxs-lookup"><span data-stu-id="0bd72-107">Description</span></span>                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="0bd72-108">**MF \_ ASFPROFILE \_ MAXPACKETSIZE**</span><span class="sxs-lookup"><span data-stu-id="0bd72-108">**MF\_ASFPROFILE\_MAXPACKETSIZE**</span></span>](mf-asfprofile-maxpacketsize-attribute.md) | <span data-ttu-id="0bd72-109">指定 ASF 檔案的封包大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0bd72-109">Specifies the maximum packet size for an ASF file, in bytes.</span></span> |
| [<span data-ttu-id="0bd72-110">**MF \_ ASFPROFILE \_ MINPACKETSIZE**</span><span class="sxs-lookup"><span data-stu-id="0bd72-110">**MF\_ASFPROFILE\_MINPACKETSIZE**</span></span>](mf-asfprofile-minpacketsize-attribute.md) | <span data-ttu-id="0bd72-111">指定 ASF 檔案的最小封包大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0bd72-111">Specifies the minimum packet size for an ASF file, in bytes.</span></span> |



 

### <a name="stream-configuration-attributes"></a><span data-ttu-id="0bd72-112">串流設定屬性</span><span class="sxs-lookup"><span data-stu-id="0bd72-112">Stream Configuration Attributes</span></span>

<span data-ttu-id="0bd72-113">下列屬性適用于 ASF 資料流程設定物件。</span><span class="sxs-lookup"><span data-stu-id="0bd72-113">The following attributes apply to the ASF stream configuration object.</span></span>



| <span data-ttu-id="0bd72-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0bd72-114">Attribute</span></span>                                                                              | <span data-ttu-id="0bd72-115">描述</span><span class="sxs-lookup"><span data-stu-id="0bd72-115">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="0bd72-116">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="0bd72-116">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md) | <span data-ttu-id="0bd72-117">設定用來編碼 Windows Media 檔案的平均 "有漏洞 bucket" 參數。</span><span class="sxs-lookup"><span data-stu-id="0bd72-117">Sets the average "leaky bucket" parameters for encoding a Windows Media file.</span></span> |
| [<span data-ttu-id="0bd72-118">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="0bd72-118">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md) | <span data-ttu-id="0bd72-119">設定用來編碼 Windows Media 檔案的尖峰 "有漏洞 bucket" 參數。</span><span class="sxs-lookup"><span data-stu-id="0bd72-119">Sets the peak "leaky bucket" parameters for encoding a Windows Media file.</span></span>    |



 

### <a name="media-buffer-attributes"></a><span data-ttu-id="0bd72-120">媒體緩衝區屬性</span><span class="sxs-lookup"><span data-stu-id="0bd72-120">Media Buffer Attributes</span></span>

<span data-ttu-id="0bd72-121">下列屬性適用于 ASF 封包的媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0bd72-121">The following attributes apply to media buffers for ASF packets.</span></span>



| <span data-ttu-id="0bd72-122">屬性</span><span class="sxs-lookup"><span data-stu-id="0bd72-122">Attribute</span></span>                                                                          | <span data-ttu-id="0bd72-123">描述</span><span class="sxs-lookup"><span data-stu-id="0bd72-123">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bd72-124">**MFASFSPLITTER 封 \_ 包 \_ 界限**</span><span class="sxs-lookup"><span data-stu-id="0bd72-124">**MFASFSPLITTER\_PACKET\_BOUNDARY**</span></span>](mfasfsplitter-packet-boundary-attribute.md) | <span data-ttu-id="0bd72-125">指定緩衝區是否包含 Advanced 系統格式的開頭 (ASF) 封包。</span><span class="sxs-lookup"><span data-stu-id="0bd72-125">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span> |



 

### <a name="presentation-descriptor-attributes"></a><span data-ttu-id="0bd72-126">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="0bd72-126">Presentation Descriptor Attributes</span></span>

<span data-ttu-id="0bd72-127">如需適用于 ASF 表示描述項的屬性清單，請參閱 [展示描述項屬性](presentation-descriptor-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="0bd72-127">For a list of attributes that apply to ASF presentation descriptors, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bd72-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="0bd72-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bd72-129">**IMFASFProfile**</span><span class="sxs-lookup"><span data-stu-id="0bd72-129">**IMFASFProfile**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[<span data-ttu-id="0bd72-130">**IMFASFStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="0bd72-130">**IMFASFStreamConfig**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[<span data-ttu-id="0bd72-131">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="0bd72-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




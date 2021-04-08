---
description: 資料流程描述元屬性
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: 資料流程描述元屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691599"
---
# <a name="stream-descriptor-attributes"></a><span data-ttu-id="e3684-103">資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="e3684-103">Stream Descriptor Attributes</span></span>

## <a name="common-stream-descriptor-attributes"></a><span data-ttu-id="e3684-104">通用資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="e3684-104">Common Stream Descriptor Attributes</span></span>

<span data-ttu-id="e3684-105">下列屬性適用于資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="e3684-105">The following attributes apply to stream descriptors.</span></span>



| <span data-ttu-id="e3684-106">屬性</span><span class="sxs-lookup"><span data-stu-id="e3684-106">Attribute</span></span>                                                   | <span data-ttu-id="e3684-107">描述</span><span class="sxs-lookup"><span data-stu-id="e3684-107">Description</span></span>                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3684-108">**MF \_ SD \_ 語言**</span><span class="sxs-lookup"><span data-stu-id="e3684-108">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)        | <span data-ttu-id="e3684-109">指定資料流程的語言。</span><span class="sxs-lookup"><span data-stu-id="e3684-109">Specifies the language for a stream.</span></span>                                                  |
| [<span data-ttu-id="e3684-110">MF \_ SD \_ 互斥 \_</span><span class="sxs-lookup"><span data-stu-id="e3684-110">MF\_SD\_MUTUALLY\_EXCLUSIVE</span></span>](mf-sd-mutually-exclusive.md) | <span data-ttu-id="e3684-111">指定資料流程是否與相同類型的其他資料流程相互排斥。</span><span class="sxs-lookup"><span data-stu-id="e3684-111">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span> |
| [<span data-ttu-id="e3684-112">**已 \_ 保護 MF SD \_**</span><span class="sxs-lookup"><span data-stu-id="e3684-112">**MF\_SD\_PROTECTED**</span></span>](mf-sd-protected-attribute.md)      | <span data-ttu-id="e3684-113">指定資料流程是否包含受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="e3684-113">Specifies whether a stream contains protected content.</span></span>                                |
| [<span data-ttu-id="e3684-114">MF \_ SD \_ STREAM \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="e3684-114">MF\_SD\_STREAM\_NAME</span></span>](mf-sd-stream-name.md)               | <span data-ttu-id="e3684-115">包含資料流程的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3684-115">Contains the name of a stream.</span></span>                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a><span data-ttu-id="e3684-116">ASF-Specific 資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="e3684-116">ASF-Specific Stream Descriptor Attributes</span></span>

<span data-ttu-id="e3684-117">下列屬性適用于 Advanced 系統格式 (ASF) 檔的資料流程描述元。</span><span class="sxs-lookup"><span data-stu-id="e3684-117">The following attributes apply to stream descriptors for Advanced Systems Format (ASF) files.</span></span>



| <span data-ttu-id="e3684-118">屬性</span><span class="sxs-lookup"><span data-stu-id="e3684-118">Attribute</span></span>                                                                                                                | <span data-ttu-id="e3684-119">描述</span><span class="sxs-lookup"><span data-stu-id="e3684-119">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3684-120">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**</span><span class="sxs-lookup"><span data-stu-id="e3684-120">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | <span data-ttu-id="e3684-121">指定在 ASF 檔案中資料流程所需的平均緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e3684-121">Specifies the average buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="e3684-122">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="e3684-122">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | <span data-ttu-id="e3684-123">在 ASF 檔案中指定資料流程的平均資料位元速率，以每秒位數表示。</span><span class="sxs-lookup"><span data-stu-id="e3684-123">Specifies the average data bit rate of a stream in an ASF file, in bits per second.</span></span>        |
| [<span data-ttu-id="e3684-124">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 語言 \_ 識別碼 \_ 索引**</span><span class="sxs-lookup"><span data-stu-id="e3684-124">**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**</span></span>](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | <span data-ttu-id="e3684-125">在 ASF 檔案中指定資料流程所使用的語言。</span><span class="sxs-lookup"><span data-stu-id="e3684-125">Specifies the language used by a stream in an ASF file.</span></span>                                    |
| [<span data-ttu-id="e3684-126">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 最大的 \_ BUFFERSIZE**</span><span class="sxs-lookup"><span data-stu-id="e3684-126">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | <span data-ttu-id="e3684-127">指定 ASF 檔案中資料流程所需的緩衝區大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e3684-127">Specifies the maximum buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="e3684-128">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 最大 \_ 資料 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="e3684-128">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | <span data-ttu-id="e3684-129">指定 ASF 檔案中資料流程的最大資料位速率（以每秒位數為單位）</span><span class="sxs-lookup"><span data-stu-id="e3684-129">Specifies the maximum data bit rate of a stream in an ASF file, in bits per second</span></span>         |
| [<span data-ttu-id="e3684-130">**MF \_ SD \_ ASF \_ 中繼資料 \_ 裝置 \_ 一致性 \_ 範本**</span><span class="sxs-lookup"><span data-stu-id="e3684-130">**MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE**</span></span>](mf-sd-asf-metadata-device-conformance-template-attribute.md) | <span data-ttu-id="e3684-131">針對 ASF 檔案中的資料流程指定裝置一致性範本，以每秒位數為單位。</span><span class="sxs-lookup"><span data-stu-id="e3684-131">Specifies the device conformance template for a stream in an ASF file, in bits per second.</span></span> |
| [<span data-ttu-id="e3684-132">**MF \_ SD \_ ASF \_ STREAMBITRATES \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="e3684-132">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | <span data-ttu-id="e3684-133">在 ASF 檔案中指定資料流程的平均位元速率，以每秒位數表示。</span><span class="sxs-lookup"><span data-stu-id="e3684-133">Specifies the average bit rate of a stream in an ASF file, in bits per second.</span></span>             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a><span data-ttu-id="e3684-134">薩米文媒體來源串流描述元屬性</span><span class="sxs-lookup"><span data-stu-id="e3684-134">SAMI Media Source Stream Descriptor Attributes</span></span>

<span data-ttu-id="e3684-135">下列屬性適用于薩米文媒體來源的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="e3684-135">The following attribute applies to the stream descriptor for the SAMI media source.</span></span>



| <span data-ttu-id="e3684-136">屬性</span><span class="sxs-lookup"><span data-stu-id="e3684-136">Attribute</span></span>                                                       | <span data-ttu-id="e3684-137">描述</span><span class="sxs-lookup"><span data-stu-id="e3684-137">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3684-138">**MF \_ SD \_ 薩米文 \_ 語言**</span><span class="sxs-lookup"><span data-stu-id="e3684-138">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="e3684-139">包含針對資料流程所定義的已同步可存取媒體交換 (薩米) 語言名稱。</span><span class="sxs-lookup"><span data-stu-id="e3684-139">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e3684-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3684-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3684-141">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e3684-141">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="e3684-142">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="e3684-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




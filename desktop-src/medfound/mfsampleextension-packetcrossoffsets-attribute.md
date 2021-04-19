---
description: 指定受保護範例框架中裝載界限的位移。
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: 'MFSampleExtension_PacketCrossOffsets 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416f41fef9caab3d73c2bdd015d345452ccbd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982301"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a><span data-ttu-id="21a75-103">MFSampleExtension \_ PacketCrossOffsets 屬性</span><span class="sxs-lookup"><span data-stu-id="21a75-103">MFSampleExtension\_PacketCrossOffsets attribute</span></span>

<span data-ttu-id="21a75-104">指定受保護範例框架中裝載界限的位移。</span><span class="sxs-lookup"><span data-stu-id="21a75-104">Specifies the offsets to the payload boundaries in a frame for protected samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="21a75-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="21a75-105">Data type</span></span>

<span data-ttu-id="21a75-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="21a75-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="21a75-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="21a75-107">Get/set</span></span>

<span data-ttu-id="21a75-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。</span><span class="sxs-lookup"><span data-stu-id="21a75-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="21a75-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。</span><span class="sxs-lookup"><span data-stu-id="21a75-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="21a75-110">適用於</span><span class="sxs-lookup"><span data-stu-id="21a75-110">Applies to</span></span>

[<span data-ttu-id="21a75-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="21a75-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="21a75-112">備註</span><span class="sxs-lookup"><span data-stu-id="21a75-112">Remarks</span></span>

<span data-ttu-id="21a75-113">此屬性適用于受 Windows Media 數位 Rights Management (DRM) 保護的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="21a75-113">This attribute applies to media samples protected by Windows Media Digital Rights Management (DRM).</span></span> <span data-ttu-id="21a75-114">屬性的值是 **DWORD** s 的陣列。</span><span class="sxs-lookup"><span data-stu-id="21a75-114">The value of the attribute is an array of **DWORD** s.</span></span> <span data-ttu-id="21a75-115">陣列中的每個專案都是裝載界限的位移（相對於框架的開頭）。</span><span class="sxs-lookup"><span data-stu-id="21a75-115">Each entry in the array is the offset of a payload boundary, relative to the start of the frame.</span></span> <span data-ttu-id="21a75-116">應用程式在解密和重建框架時可以使用這些值。</span><span class="sxs-lookup"><span data-stu-id="21a75-116">An application can use these values when decrypting and reconstructing the frames.</span></span>

<span data-ttu-id="21a75-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="21a75-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="21a75-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="21a75-118">Requirements</span></span>



| <span data-ttu-id="21a75-119">需求</span><span class="sxs-lookup"><span data-stu-id="21a75-119">Requirement</span></span> | <span data-ttu-id="21a75-120">值</span><span class="sxs-lookup"><span data-stu-id="21a75-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21a75-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21a75-121">Minimum supported client</span></span><br/> | <span data-ttu-id="21a75-122">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21a75-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="21a75-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21a75-123">Minimum supported server</span></span><br/> | <span data-ttu-id="21a75-124">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21a75-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="21a75-125">標頭</span><span class="sxs-lookup"><span data-stu-id="21a75-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="21a75-126"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="21a75-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21a75-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21a75-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a75-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="21a75-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="21a75-129">ASF 分隔器</span><span class="sxs-lookup"><span data-stu-id="21a75-129">ASF Splitter</span></span>](asf-splitter.md)
</dt> <dt>

[<span data-ttu-id="21a75-130">範例屬性</span><span class="sxs-lookup"><span data-stu-id="21a75-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="21a75-131">媒體範例</span><span class="sxs-lookup"><span data-stu-id="21a75-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 





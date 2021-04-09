---
description: 包含以硬體為基礎的媒體基礎轉換 (MFT) 上連接資料流程的資料流程屬性指標。
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: 'MFT_CONNECTED_STREAM_ATTRIBUTE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848713"
---
# <a name="mft_connected_stream_attribute-attribute"></a><span data-ttu-id="9384b-103">MFT \_ 連接的 \_ 資料流程 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="9384b-103">MFT\_CONNECTED\_STREAM\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="9384b-104">包含以硬體為基礎的媒體基礎轉換 (MFT) 上連接資料流程的資料流程屬性指標。</span><span class="sxs-lookup"><span data-stu-id="9384b-104">Contains a pointer to the stream attributes of the connected stream on a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="9384b-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9384b-105">Data type</span></span>

<span data-ttu-id="9384b-106">**IMFAttributes \** _ 儲存為 _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="9384b-106">**IMFAttributes\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="9384b-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="9384b-107">Get/set</span></span>

<span data-ttu-id="9384b-108">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="9384b-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="9384b-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="9384b-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="9384b-110">備註</span><span class="sxs-lookup"><span data-stu-id="9384b-110">Remarks</span></span>

<span data-ttu-id="9384b-111">應用程式通常不會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="9384b-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="9384b-112">這個屬性會用於作為硬體裝置之 proxy 的 MFTs。</span><span class="sxs-lookup"><span data-stu-id="9384b-112">This attribute is used for MFTs that act as proxies to a hardware device.</span></span> <span data-ttu-id="9384b-113">如需詳細資訊，請參閱 [硬體 MFTs](hardware-mfts.md)。</span><span class="sxs-lookup"><span data-stu-id="9384b-113">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>

<span data-ttu-id="9384b-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="9384b-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9384b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9384b-115">Requirements</span></span>



| <span data-ttu-id="9384b-116">需求</span><span class="sxs-lookup"><span data-stu-id="9384b-116">Requirement</span></span> | <span data-ttu-id="9384b-117">值</span><span class="sxs-lookup"><span data-stu-id="9384b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9384b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9384b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9384b-119">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9384b-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="9384b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9384b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9384b-121">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9384b-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9384b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9384b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9384b-123"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="9384b-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9384b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9384b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9384b-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9384b-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9384b-126">\_連接 \_ 至 \_ HW \_ 串流的 MFT</span><span class="sxs-lookup"><span data-stu-id="9384b-126">MFT\_CONNECTED\_TO\_HW\_STREAM</span></span>](mft-connected-to-hw-stream.md)
</dt> <dt>

[<span data-ttu-id="9384b-127">硬體 MFTs</span><span class="sxs-lookup"><span data-stu-id="9384b-127">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="9384b-128">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="9384b-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 





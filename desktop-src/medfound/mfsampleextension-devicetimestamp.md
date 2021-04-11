---
description: 包含設備磁碟機的時間戳記。
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: 'MFSampleExtension_DeviceTimestamp 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b354ecd0e399fc297d3677d29b88847f9eba8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848718"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a><span data-ttu-id="3de1e-103">MFSampleExtension \_ DeviceTimestamp 屬性</span><span class="sxs-lookup"><span data-stu-id="3de1e-103">MFSampleExtension\_DeviceTimestamp attribute</span></span>

<span data-ttu-id="3de1e-104">包含設備磁碟機的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="3de1e-104">Contains the time stamp from the device driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="3de1e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3de1e-105">Data type</span></span>

<span data-ttu-id="3de1e-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="3de1e-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="3de1e-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="3de1e-107">Get/set</span></span>

<span data-ttu-id="3de1e-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。</span><span class="sxs-lookup"><span data-stu-id="3de1e-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="3de1e-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。</span><span class="sxs-lookup"><span data-stu-id="3de1e-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3de1e-110">適用於</span><span class="sxs-lookup"><span data-stu-id="3de1e-110">Applies to</span></span>

[<span data-ttu-id="3de1e-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="3de1e-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="3de1e-112">備註</span><span class="sxs-lookup"><span data-stu-id="3de1e-112">Remarks</span></span>

<span data-ttu-id="3de1e-113">這個屬性是在由捕獲裝置的媒體來源所建立的媒體範例上設定的。</span><span class="sxs-lookup"><span data-stu-id="3de1e-113">This attribute is set on media samples created by a media source for a capture device.</span></span> <span data-ttu-id="3de1e-114">這個屬性的值是在 [**MFTIME**](mftime.md) 網域中，與 query 效能計數器共用 EPOCH (QPC) 時間，而且一律以100ns 單位表示。</span><span class="sxs-lookup"><span data-stu-id="3de1e-114">This attribute's value is in the [**MFTIME**](mftime.md) domain, sharing an epoch with query performance counter (QPC) time and always expressed in 100ns units.</span></span> <span data-ttu-id="3de1e-115">這個屬性可用於插入至 capture 管線的 MFTs。</span><span class="sxs-lookup"><span data-stu-id="3de1e-115">This attribute is available for MFTs inserted into the capture pipeline.</span></span>

<span data-ttu-id="3de1e-116">若要取得相對於資料流程開頭的時間戳記，請呼叫 [**IMFSample：： GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) 方法。</span><span class="sxs-lookup"><span data-stu-id="3de1e-116">To get the time stamp relative to the start of streaming, call the [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) method.</span></span>

<span data-ttu-id="3de1e-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="3de1e-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3de1e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3de1e-118">Requirements</span></span>



| <span data-ttu-id="3de1e-119">需求</span><span class="sxs-lookup"><span data-stu-id="3de1e-119">Requirement</span></span> | <span data-ttu-id="3de1e-120">值</span><span class="sxs-lookup"><span data-stu-id="3de1e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3de1e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3de1e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3de1e-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3de1e-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3de1e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3de1e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3de1e-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3de1e-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3de1e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3de1e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3de1e-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3de1e-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de1e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3de1e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de1e-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3de1e-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3de1e-129">媒體基礎中的音訊/影片捕獲</span><span class="sxs-lookup"><span data-stu-id="3de1e-129">Audio/Video Capture in Media Foundation</span></span>](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="3de1e-130">範例屬性</span><span class="sxs-lookup"><span data-stu-id="3de1e-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 





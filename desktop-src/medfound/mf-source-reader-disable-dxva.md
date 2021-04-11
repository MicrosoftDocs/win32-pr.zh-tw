---
description: 指定來源讀取器是否啟用 (DXVA) 影片解碼器的 DirectX Video 加速。
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: 'MF_SOURCE_READER_DISABLE_DXVA 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320471"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a><span data-ttu-id="c6c79-103">MF \_ 來源 \_ 讀取器 \_ 停用 \_ DXVA 屬性</span><span class="sxs-lookup"><span data-stu-id="c6c79-103">MF\_SOURCE\_READER\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="c6c79-104">指定 [來源讀取器](source-reader.md) 是否啟用 (DXVA) 影片解碼器的 DirectX Video 加速。</span><span class="sxs-lookup"><span data-stu-id="c6c79-104">Specifies whether the [Source Reader](source-reader.md) enables DirectX Video Acceleration (DXVA) on the video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="c6c79-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c6c79-105">Data type</span></span>

<span data-ttu-id="c6c79-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c6c79-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c6c79-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="c6c79-107">Get/set</span></span>

<span data-ttu-id="c6c79-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="c6c79-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c6c79-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="c6c79-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6c79-110">備註</span><span class="sxs-lookup"><span data-stu-id="c6c79-110">Remarks</span></span>

<span data-ttu-id="c6c79-111">如果下列條件成立，則適用此屬性：</span><span class="sxs-lookup"><span data-stu-id="c6c79-111">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="c6c79-112">來源讀取器會解碼影片串流。</span><span class="sxs-lookup"><span data-stu-id="c6c79-112">The source reader decodes a video stream.</span></span>
-   <span data-ttu-id="c6c79-113">影片解碼支援 DXVA 解碼。</span><span class="sxs-lookup"><span data-stu-id="c6c79-113">The video decoder supports DXVA decoding.</span></span>
-   <span data-ttu-id="c6c79-114">應用程式會使用 [MF \_ 來源讀取器的「 \_ \_ D3D \_ 管理員](mf-source-reader-d3d-manager.md) 」屬性來設定來源讀取器上的 [Direct3D 裝置管理員](direct3d-device-manager.md) 。</span><span class="sxs-lookup"><span data-stu-id="c6c79-114">The application uses the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute to set the [Direct3D Device Manager](direct3d-device-manager.md) on the source reader.</span></span>

<span data-ttu-id="c6c79-115">這個屬性可讓應用程式停用 DXVA，同時仍在對 Direct3D 介面進行解碼。</span><span class="sxs-lookup"><span data-stu-id="c6c79-115">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="c6c79-116">根據預設，來源讀取器使用 [Direct3D 裝置管理員](direct3d-device-manager.md) 有兩個用途：</span><span class="sxs-lookup"><span data-stu-id="c6c79-116">By default, the source reader uses the [Direct3D Device Manager](direct3d-device-manager.md) for two purposes:</span></span>

-   <span data-ttu-id="c6c79-117">啟用影片解碼中的 DXVA 解碼。</span><span class="sxs-lookup"><span data-stu-id="c6c79-117">To enable DXVA decoding in the video decoder.</span></span>
-   <span data-ttu-id="c6c79-118">為影片範例配置 Direct3D 介面。</span><span class="sxs-lookup"><span data-stu-id="c6c79-118">To allocate Direct3D surfaces for the video samples.</span></span>

<span data-ttu-id="c6c79-119">如果 MF \_ 來源讀取器的值 \_ \_ 停 \_ 用 DXVA 屬性為 **TRUE**，則來源讀取器將會停用 DXVA 解碼，不過它仍然會使用 [direct3d 裝置管理員](direct3d-device-manager.md) 來配置 direct3d 表面。</span><span class="sxs-lookup"><span data-stu-id="c6c79-119">If the value of the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is **TRUE**, the source reader does disables DXVA decoding, although it still uses the [Direct3D Device Manager](direct3d-device-manager.md) to allocate Direct3D surfaces.</span></span>

<span data-ttu-id="c6c79-120">如果未設定 [Mf 來源讀取器] 的 [ [ \_ \_ \_ D3D \_ 管理員](mf-source-reader-d3d-manager.md) ] 屬性，則 \_ 會忽略 [mf 來源讀取器] 停用 \_ \_ \_ DXVA 屬性。</span><span class="sxs-lookup"><span data-stu-id="c6c79-120">If the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute is not set, the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is ignored.</span></span>

<span data-ttu-id="c6c79-121">這個屬性的預設值為 **FALSE**，表示 DXVA 解碼會在可用時啟用。</span><span class="sxs-lookup"><span data-stu-id="c6c79-121">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c79-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6c79-122">Requirements</span></span>



| <span data-ttu-id="c6c79-123">需求</span><span class="sxs-lookup"><span data-stu-id="c6c79-123">Requirement</span></span> | <span data-ttu-id="c6c79-124">值</span><span class="sxs-lookup"><span data-stu-id="c6c79-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c79-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6c79-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c79-126">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6c79-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c6c79-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6c79-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c79-128">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6c79-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c6c79-129">標頭</span><span class="sxs-lookup"><span data-stu-id="c6c79-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6c79-130"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c79-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c79-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6c79-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c79-132">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c6c79-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6c79-133">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="c6c79-133">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="c6c79-134">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="c6c79-134">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 





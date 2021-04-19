---
description: 針對 YUV 媒體類型，定義從 YCbCr 色彩空間到 RGB 色彩空間的轉換矩陣。
ms.assetid: b268d16d-b4cc-4026-9ba7-805cc5409b95
title: 'MF_MT_YUV_MATRIX 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c6976e4652c69b3bddc910dcc536a3d07bf39a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980508"
---
# <a name="mf_mt_yuv_matrix-attribute"></a><span data-ttu-id="35eba-103">MF \_ MT \_ YUV \_ 矩陣屬性</span><span class="sxs-lookup"><span data-stu-id="35eba-103">MF\_MT\_YUV\_MATRIX attribute</span></span>

<span data-ttu-id="35eba-104">針對 YUV 媒體類型，定義從 Y'Cb'Cr 的色彩空間到 R'G'B 的色彩空間的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="35eba-104">For YUV media types, defines the conversion matrix from the Y'Cb'Cr' color space to the R'G'B' color space.</span></span>

## <a name="data-type"></a><span data-ttu-id="35eba-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="35eba-105">Data type</span></span>

<span data-ttu-id="35eba-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="35eba-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="35eba-107">備註</span><span class="sxs-lookup"><span data-stu-id="35eba-107">Remarks</span></span>

<span data-ttu-id="35eba-108">這個屬性的值是 [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="35eba-108">The value of this attribute is a member of the [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) enumeration.</span></span>

<span data-ttu-id="35eba-109">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="35eba-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="35eba-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="35eba-110">Requirements</span></span>



| <span data-ttu-id="35eba-111">需求</span><span class="sxs-lookup"><span data-stu-id="35eba-111">Requirement</span></span> | <span data-ttu-id="35eba-112">值</span><span class="sxs-lookup"><span data-stu-id="35eba-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35eba-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35eba-113">Minimum supported client</span></span><br/> | <span data-ttu-id="35eba-114">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35eba-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="35eba-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35eba-115">Minimum supported server</span></span><br/> | <span data-ttu-id="35eba-116">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35eba-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="35eba-117">標頭</span><span class="sxs-lookup"><span data-stu-id="35eba-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="35eba-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="35eba-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35eba-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35eba-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35eba-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="35eba-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="35eba-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="35eba-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="35eba-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="35eba-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="35eba-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="35eba-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="35eba-124">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="35eba-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="35eba-125">擴充的色彩資訊</span><span class="sxs-lookup"><span data-stu-id="35eba-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 





---
description: 指定媒體類型中每個樣本的大小（以位元組為單位）。
ms.assetid: 4c28f73d-ff40-4eb9-a45f-57a60df719c6
title: 'MF_MT_SAMPLE_SIZE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bb897524dac5f73f4d4553f8e77e02ef473f611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978863"
---
# <a name="mf_mt_sample_size-attribute"></a><span data-ttu-id="60d4d-103">MF \_ MT \_ 範例 \_ 大小屬性</span><span class="sxs-lookup"><span data-stu-id="60d4d-103">MF\_MT\_SAMPLE\_SIZE attribute</span></span>

<span data-ttu-id="60d4d-104">指定媒體類型中每個樣本的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="60d4d-104">Specifies the size of each sample, in bytes, in a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="60d4d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="60d4d-105">Data type</span></span>

<span data-ttu-id="60d4d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="60d4d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="60d4d-107">備註</span><span class="sxs-lookup"><span data-stu-id="60d4d-107">Remarks</span></span>

<span data-ttu-id="60d4d-108">只有當 [**MF \_ MT \_ 固定 \_ 大小 \_ 範例**](mf-mt-fixed-size-samples-attribute.md) 屬性為 **TRUE** 時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="60d4d-108">This attribute is valid only if the [**MF\_MT\_FIXED\_SIZE\_SAMPLES**](mf-mt-fixed-size-samples-attribute.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="60d4d-109">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="60d4d-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="60d4d-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="60d4d-110">Requirements</span></span>



| <span data-ttu-id="60d4d-111">需求</span><span class="sxs-lookup"><span data-stu-id="60d4d-111">Requirement</span></span> | <span data-ttu-id="60d4d-112">值</span><span class="sxs-lookup"><span data-stu-id="60d4d-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60d4d-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60d4d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="60d4d-114">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60d4d-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="60d4d-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60d4d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="60d4d-116">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60d4d-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="60d4d-117">標頭</span><span class="sxs-lookup"><span data-stu-id="60d4d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="60d4d-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="60d4d-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d4d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60d4d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d4d-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="60d4d-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="60d4d-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="60d4d-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="60d4d-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="60d4d-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="60d4d-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="60d4d-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="60d4d-124">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="60d4d-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 





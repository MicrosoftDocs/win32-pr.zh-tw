---
description: 影片輔助 (VAUX 數位視訊中) 的原始檔控制套件 (DV) 媒體類型。
ms.assetid: 14098435-5033-489c-908f-cbb814a0349c
title: 'MF_MT_DV_VAUX_CTRL_PACK 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4fc8e8eeeab10936e42cfba96693aa9097c1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026440"
---
# <a name="mf_mt_dv_vaux_ctrl_pack-attribute"></a><span data-ttu-id="ffe5e-103">MF \_ MT \_ DV \_ VAUX \_ CTRL \_ PACK 屬性</span><span class="sxs-lookup"><span data-stu-id="ffe5e-103">MF\_MT\_DV\_VAUX\_CTRL\_PACK attribute</span></span>

<span data-ttu-id="ffe5e-104">影片輔助 (VAUX 數位視訊中) 的原始檔控制套件 (DV) 媒體類型。</span><span class="sxs-lookup"><span data-stu-id="ffe5e-104">Video auxiliary (VAUX) source control pack in a digital video (DV) media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="ffe5e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ffe5e-105">Data type</span></span>

<span data-ttu-id="ffe5e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ffe5e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ffe5e-107">備註</span><span class="sxs-lookup"><span data-stu-id="ffe5e-107">Remarks</span></span>

<span data-ttu-id="ffe5e-108">這個屬性會對應至 DirectShow [**DVINFO**](/windows/win32/api/strmif/ns-strmif-dvinfo)結構的 **dwDVVAuxCtl** 成員。</span><span class="sxs-lookup"><span data-stu-id="ffe5e-108">This attribute corresponds to the **dwDVVAuxCtl** member of the DirectShow [**DVINFO**](/windows/win32/api/strmif/ns-strmif-dvinfo) structure.</span></span>

<span data-ttu-id="ffe5e-109">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="ffe5e-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe5e-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffe5e-110">Requirements</span></span>



| <span data-ttu-id="ffe5e-111">需求</span><span class="sxs-lookup"><span data-stu-id="ffe5e-111">Requirement</span></span> | <span data-ttu-id="ffe5e-112">值</span><span class="sxs-lookup"><span data-stu-id="ffe5e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe5e-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffe5e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ffe5e-114">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffe5e-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ffe5e-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffe5e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ffe5e-116">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffe5e-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ffe5e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="ffe5e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffe5e-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ffe5e-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffe5e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffe5e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe5e-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ffe5e-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ffe5e-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ffe5e-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ffe5e-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ffe5e-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ffe5e-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ffe5e-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ffe5e-124">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="ffe5e-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 

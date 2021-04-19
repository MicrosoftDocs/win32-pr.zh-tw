---
description: 音訊輔助 (AAUX 數位視訊中第二個音訊區塊的) 原始檔控制套件 (DV) 媒體類型。
ms.assetid: e9c17940-beb7-4034-95a3-983aaca0c905
title: 'MF_MT_DV_AAUX_CTRL_PACK_1 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 119c58d6a988f955229b46c0cb482bc24dd6f770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985174"
---
# <a name="mf_mt_dv_aaux_ctrl_pack_1-attribute"></a><span data-ttu-id="12e76-103">MF \_ MT \_ DV \_ AAUX \_ CTRL \_ PACK \_ 1 屬性</span><span class="sxs-lookup"><span data-stu-id="12e76-103">MF\_MT\_DV\_AAUX\_CTRL\_PACK\_1 attribute</span></span>

<span data-ttu-id="12e76-104">音訊輔助 (AAUX 數位視訊中第二個音訊區塊的) 原始檔控制套件 (DV) 媒體類型。</span><span class="sxs-lookup"><span data-stu-id="12e76-104">Audio auxiliary (AAUX) source control pack for the second audio block in a digital video (DV) media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="12e76-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="12e76-105">Data type</span></span>

<span data-ttu-id="12e76-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="12e76-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="12e76-107">備註</span><span class="sxs-lookup"><span data-stu-id="12e76-107">Remarks</span></span>

<span data-ttu-id="12e76-108">這個屬性會對應至 DirectShow [**DVINFO**](/windows/win32/api/strmif/ns-strmif-dvinfo)結構的 **dwDVAAuxCtl1** 成員。</span><span class="sxs-lookup"><span data-stu-id="12e76-108">This attribute corresponds to the **dwDVAAuxCtl1** member of the DirectShow [**DVINFO**](/windows/win32/api/strmif/ns-strmif-dvinfo) structure.</span></span>

<span data-ttu-id="12e76-109">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="12e76-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="12e76-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="12e76-110">Requirements</span></span>



| <span data-ttu-id="12e76-111">需求</span><span class="sxs-lookup"><span data-stu-id="12e76-111">Requirement</span></span> | <span data-ttu-id="12e76-112">值</span><span class="sxs-lookup"><span data-stu-id="12e76-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="12e76-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12e76-113">Minimum supported client</span></span><br/> | <span data-ttu-id="12e76-114">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12e76-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="12e76-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12e76-115">Minimum supported server</span></span><br/> | <span data-ttu-id="12e76-116">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12e76-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="12e76-117">標頭</span><span class="sxs-lookup"><span data-stu-id="12e76-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="12e76-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="12e76-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e76-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12e76-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e76-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="12e76-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="12e76-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="12e76-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="12e76-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="12e76-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="12e76-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="12e76-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="12e76-124">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="12e76-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 

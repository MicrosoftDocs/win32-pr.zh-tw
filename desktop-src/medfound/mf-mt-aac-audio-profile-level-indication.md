---
description: 指定 (AAC) 串流之 Advanced Audio 編碼的音訊設定檔和層級。
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: 'MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116bfc2b41cff3cbd92fc9a60be150ea598e1cc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984837"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a><span data-ttu-id="986e6-103">MF \_ MT \_ AAC \_ 音訊 \_ 設定檔 \_ 層級 \_ 指示屬性</span><span class="sxs-lookup"><span data-stu-id="986e6-103">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION attribute</span></span>

<span data-ttu-id="986e6-104">指定 (AAC) 串流之 Advanced Audio 編碼的音訊設定檔和層級。</span><span class="sxs-lookup"><span data-stu-id="986e6-104">Specifies the audio profile and level of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="986e6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="986e6-105">Data type</span></span>

<span data-ttu-id="986e6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="986e6-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="986e6-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="986e6-107">Get/set</span></span>

<span data-ttu-id="986e6-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="986e6-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="986e6-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="986e6-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="986e6-110">套用至</span><span class="sxs-lookup"><span data-stu-id="986e6-110">Applies To</span></span>

[<span data-ttu-id="986e6-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="986e6-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="986e6-112">備註</span><span class="sxs-lookup"><span data-stu-id="986e6-112">Remarks</span></span>

<span data-ttu-id="986e6-113">此屬性包含 **audioProfileLevelIndication** 欄位的值，如 ISO/IEC 14496-3 所定義。</span><span class="sxs-lookup"><span data-stu-id="986e6-113">This attribute contains the value of the **audioProfileLevelIndication** field, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="986e6-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="986e6-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="986e6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="986e6-115">Requirements</span></span>



| <span data-ttu-id="986e6-116">需求</span><span class="sxs-lookup"><span data-stu-id="986e6-116">Requirement</span></span> | <span data-ttu-id="986e6-117">值</span><span class="sxs-lookup"><span data-stu-id="986e6-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="986e6-118">標頭</span><span class="sxs-lookup"><span data-stu-id="986e6-118">Header</span></span><br/> | <dl> <span data-ttu-id="986e6-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="986e6-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="986e6-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="986e6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="986e6-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="986e6-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="986e6-122">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="986e6-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 





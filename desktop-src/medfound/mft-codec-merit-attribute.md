---
description: 包含硬體編解碼器的業績值。
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: 'MFT_CODEC_MERIT_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993019"
---
# <a name="mft_codec_merit_attribute-attribute"></a><span data-ttu-id="3cf7e-103">MFT \_ 編解碼器的 \_ 業績 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="3cf7e-103">MFT\_CODEC\_MERIT\_Attribute attribute</span></span>

<span data-ttu-id="3cf7e-104">包含硬體編解碼器的業績值。</span><span class="sxs-lookup"><span data-stu-id="3cf7e-104">Contains the merit value of a hardware codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="3cf7e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3cf7e-105">Data type</span></span>

<span data-ttu-id="3cf7e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3cf7e-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3cf7e-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="3cf7e-107">Get/set</span></span>

<span data-ttu-id="3cf7e-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="3cf7e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3cf7e-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="3cf7e-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="3cf7e-110">備註</span><span class="sxs-lookup"><span data-stu-id="3cf7e-110">Remarks</span></span>

<span data-ttu-id="3cf7e-111">這個屬性是在代表硬體編解碼器的媒體基礎轉換 (MFT) 的啟用物件上設定的。</span><span class="sxs-lookup"><span data-stu-id="3cf7e-111">This attribute is set on the activation object for a Media Foundation transform (MFT) that represents a hardware codec.</span></span> <span data-ttu-id="3cf7e-112">屬性的值是編解碼器的業績值。</span><span class="sxs-lookup"><span data-stu-id="3cf7e-112">The value of the attribute is the codec's merit value.</span></span>

<span data-ttu-id="3cf7e-113">如果設定了 **MFT \_ 列舉 \_ 旗標 \_ SORTANDFILTER** 旗標，則此屬性會控制 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式列舉編解碼器的順序。</span><span class="sxs-lookup"><span data-stu-id="3cf7e-113">This attribute controls the order in which the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function enumerates codecs, if the **MFT\_ENUM\_FLAG\_SORTANDFILTER** flag is set.</span></span> <span data-ttu-id="3cf7e-114">具有值的 MFTs 在清單中會比其他 MFTs 更高。</span><span class="sxs-lookup"><span data-stu-id="3cf7e-114">MFTs with a merit value appear higher in the list than other MFTs.</span></span>

<span data-ttu-id="3cf7e-115">這個屬性不包含受信任的值。</span><span class="sxs-lookup"><span data-stu-id="3cf7e-115">This attribute does not contain a trusted value.</span></span> <span data-ttu-id="3cf7e-116">若要驗證編解碼器的實際值，請呼叫 [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) 函數。</span><span class="sxs-lookup"><span data-stu-id="3cf7e-116">To verify the codec's actual merit value, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span>

<span data-ttu-id="3cf7e-117">如果 MFT 編解碼器的 [使用規定] 屬性的值 \_ \_ \_ 與 [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)所抓取的 [使用] 值不符， [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 方法將會失敗，並傳回 **MF \_ E \_ 不正確 \_ 編解碼器 \_**。</span><span class="sxs-lookup"><span data-stu-id="3cf7e-117">If the value of the MFT\_CODEC\_MERIT\_Attribute attribute does not match the merit value retrieved by [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails and returns **MF\_E\_INVALID\_CODEC\_MERIT**.</span></span>

<span data-ttu-id="3cf7e-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="3cf7e-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cf7e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cf7e-119">Requirements</span></span>



| <span data-ttu-id="3cf7e-120">需求</span><span class="sxs-lookup"><span data-stu-id="3cf7e-120">Requirement</span></span> | <span data-ttu-id="3cf7e-121">值</span><span class="sxs-lookup"><span data-stu-id="3cf7e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf7e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cf7e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf7e-123">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cf7e-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="3cf7e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cf7e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf7e-125">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cf7e-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3cf7e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3cf7e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cf7e-127"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cf7e-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cf7e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cf7e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf7e-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3cf7e-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3cf7e-130">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="3cf7e-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 





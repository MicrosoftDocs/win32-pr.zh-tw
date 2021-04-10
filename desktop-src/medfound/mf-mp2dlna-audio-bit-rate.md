---
description: 指定數位客廳網路聯盟 (DLNA) 媒體接收器的最大音訊位速度。
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: 'MF_MP2DLNA_AUDIO_BIT_RATE 屬性 (Mfmp2dlna) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c61554f592aefbb863057339d807e23fc96567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943786"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a><span data-ttu-id="7965d-103">MF \_ MP2DLNA \_ 音訊 \_ 位 \_ 速率屬性</span><span class="sxs-lookup"><span data-stu-id="7965d-103">MF\_MP2DLNA\_AUDIO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="7965d-104">指定數位客廳網路聯盟 (DLNA) 媒體接收器的最大音訊位速度。</span><span class="sxs-lookup"><span data-stu-id="7965d-104">Specifies the maximum audio bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="7965d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7965d-105">Data type</span></span>

<span data-ttu-id="7965d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7965d-106">**UINT32**</span></span>

<span data-ttu-id="7965d-107">值是編碼音訊串流的目標最大位元速率，以每秒位數為單位。</span><span class="sxs-lookup"><span data-stu-id="7965d-107">The value is the target maximum bit rate for the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="7965d-108">此值必須是適用于 DLNA 的 MPEG-2 第2層音訊所允許的位元速率之一。</span><span class="sxs-lookup"><span data-stu-id="7965d-108">The value must be one of the bit rates allowed for MPEG-2 layer 2 audio for DLNA.</span></span> <span data-ttu-id="7965d-109">預設值為 192000 (192 Kbps) 。</span><span class="sxs-lookup"><span data-stu-id="7965d-109">The default value is 192000 (192 Kbps).</span></span>

## <a name="getset"></a><span data-ttu-id="7965d-110">取得/設定</span><span class="sxs-lookup"><span data-stu-id="7965d-110">Get/set</span></span>

<span data-ttu-id="7965d-111">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="7965d-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7965d-112">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="7965d-112">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7965d-113">備註</span><span class="sxs-lookup"><span data-stu-id="7965d-113">Remarks</span></span>

<span data-ttu-id="7965d-114">若要在 DLNA 媒體接收器上設定此屬性，請查詢媒體接收器以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。</span><span class="sxs-lookup"><span data-stu-id="7965d-114">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="7965d-115">開始串流之前，請設定屬性。</span><span class="sxs-lookup"><span data-stu-id="7965d-115">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="7965d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7965d-116">Requirements</span></span>



| <span data-ttu-id="7965d-117">需求</span><span class="sxs-lookup"><span data-stu-id="7965d-117">Requirement</span></span> | <span data-ttu-id="7965d-118">值</span><span class="sxs-lookup"><span data-stu-id="7965d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7965d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7965d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7965d-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7965d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7965d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7965d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7965d-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7965d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7965d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7965d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7965d-124"><dt>Mfmp2dlna。h</dt></span><span class="sxs-lookup"><span data-stu-id="7965d-124"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7965d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7965d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7965d-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7965d-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





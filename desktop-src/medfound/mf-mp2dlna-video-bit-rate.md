---
description: 指定數位客廳網路聯盟 (DLNA) 媒體接收器的最大視頻位元速率。
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: 'MF_MP2DLNA_VIDEO_BIT_RATE 屬性 (Mfmp2dlna) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191892"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a><span data-ttu-id="0094c-103">MF \_ MP2DLNA \_ 影片 \_ 位 \_ 速率屬性</span><span class="sxs-lookup"><span data-stu-id="0094c-103">MF\_MP2DLNA\_VIDEO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="0094c-104">指定數位客廳網路聯盟 (DLNA) 媒體接收器的最大視頻位元速率。</span><span class="sxs-lookup"><span data-stu-id="0094c-104">Specifies the maximum video bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="0094c-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="0094c-105">Data type</span></span>

<span data-ttu-id="0094c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0094c-106">**UINT32**</span></span>

<span data-ttu-id="0094c-107">值是編碼影片串流的目標最大位元速率，以每秒位數為單位。</span><span class="sxs-lookup"><span data-stu-id="0094c-107">The value is the target maximum bit rate for the encoded video stream, in bits per second.</span></span> <span data-ttu-id="0094c-108">最大值為 9800000 (9.8 Mbps) ，這也是預設值。</span><span class="sxs-lookup"><span data-stu-id="0094c-108">The maximum value is 9800000 (9.8 Mbps), which is also the default value.</span></span>

## <a name="getset"></a><span data-ttu-id="0094c-109">取得/設定</span><span class="sxs-lookup"><span data-stu-id="0094c-109">Get/set</span></span>

<span data-ttu-id="0094c-110">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="0094c-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0094c-111">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="0094c-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="0094c-112">備註</span><span class="sxs-lookup"><span data-stu-id="0094c-112">Remarks</span></span>

<span data-ttu-id="0094c-113">若要在 DLNA 媒體接收器上設定此屬性，請查詢媒體接收器以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。</span><span class="sxs-lookup"><span data-stu-id="0094c-113">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="0094c-114">開始串流之前，請設定屬性。</span><span class="sxs-lookup"><span data-stu-id="0094c-114">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="0094c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0094c-115">Requirements</span></span>



| <span data-ttu-id="0094c-116">需求</span><span class="sxs-lookup"><span data-stu-id="0094c-116">Requirement</span></span> | <span data-ttu-id="0094c-117">值</span><span class="sxs-lookup"><span data-stu-id="0094c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0094c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0094c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0094c-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0094c-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0094c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0094c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0094c-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0094c-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0094c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0094c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0094c-123"><dt>Mfmp2dlna。h</dt></span><span class="sxs-lookup"><span data-stu-id="0094c-123"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0094c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0094c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0094c-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="0094c-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





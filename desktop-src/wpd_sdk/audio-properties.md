---
description: Windows 可攜式裝置支援下列音訊屬性。
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: '音訊屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1bdab201fc987d5bc1aff3638fbb57358115fdce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992842"
---
# <a name="audio-properties"></a><span data-ttu-id="3a57f-103">音訊屬性</span><span class="sxs-lookup"><span data-stu-id="3a57f-103">Audio Properties</span></span>

<span data-ttu-id="3a57f-104">Windows 可攜式裝置支援下列音訊屬性。</span><span class="sxs-lookup"><span data-stu-id="3a57f-104">Windows Portable Devices supports the following audio properties.</span></span>



| <span data-ttu-id="3a57f-105">屬性</span><span class="sxs-lookup"><span data-stu-id="3a57f-105">Property</span></span>                         | <span data-ttu-id="3a57f-106">VarType</span><span class="sxs-lookup"><span data-stu-id="3a57f-106">VarType</span></span>     | <span data-ttu-id="3a57f-107">Description</span><span class="sxs-lookup"><span data-stu-id="3a57f-107">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a57f-108">**WPD \_ 音訊 \_ 位 \_ 深度**</span><span class="sxs-lookup"><span data-stu-id="3a57f-108">**WPD\_AUDIO\_BIT\_DEPTH**</span></span>       | <span data-ttu-id="3a57f-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="3a57f-109">**VT\_UI4**</span></span> | <span data-ttu-id="3a57f-110">音訊的位深度。</span><span class="sxs-lookup"><span data-stu-id="3a57f-110">The bit-depth of the audio.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="3a57f-111">**WPD \_ 音訊 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="3a57f-111">**WPD\_AUDIO\_BITRATE**</span></span>          | <span data-ttu-id="3a57f-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="3a57f-112">**VT\_UI4**</span></span> | <span data-ttu-id="3a57f-113">音訊的位元速率，以位/秒為單位。</span><span class="sxs-lookup"><span data-stu-id="3a57f-113">The bit rate of the audio, in bits per second.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="3a57f-114">**WPD \_ 音訊 \_ 區塊 \_ 對齊**</span><span class="sxs-lookup"><span data-stu-id="3a57f-114">**WPD\_AUDIO\_BLOCK\_ALIGNMENT**</span></span> | <span data-ttu-id="3a57f-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="3a57f-115">**VT\_UI4**</span></span> | <span data-ttu-id="3a57f-116">音訊檔案的區塊對齊（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a57f-116">The block alignment of the audio file, in bytes.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="3a57f-117">**WPD \_ 音訊 \_ 頻道 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="3a57f-117">**WPD\_AUDIO\_CHANNEL\_COUNT**</span></span>   | <span data-ttu-id="3a57f-118">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="3a57f-118">**VT\_R4**</span></span>  | <span data-ttu-id="3a57f-119">此音訊檔案中的通道數目，例如1、2或5.1。</span><span class="sxs-lookup"><span data-stu-id="3a57f-119">The number of channels in this audio file, for example, 1, 2, or 5.1.</span></span>                                                                                                                                              |
| <span data-ttu-id="3a57f-120">**WPD \_ 音訊 \_ 格式 \_ 代碼**</span><span class="sxs-lookup"><span data-stu-id="3a57f-120">**WPD\_AUDIO\_FORMAT\_CODE**</span></span>     | <span data-ttu-id="3a57f-121">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="3a57f-121">**VT\_UI4**</span></span> | <span data-ttu-id="3a57f-122">註冊的 WAVE 格式代碼編號。</span><span class="sxs-lookup"><span data-stu-id="3a57f-122">The registered WAVE format code number.</span></span> <span data-ttu-id="3a57f-123">如需註冊的 WAVE 格式清單，請參閱 MSDN 網站上的 [註冊的 FOURCC 碼和 WAVE 格式](https://msdn2.microsoft.com/library/ms867195.aspx) 文章。</span><span class="sxs-lookup"><span data-stu-id="3a57f-123">For a listing of registered WAVE formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3a57f-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a57f-124">Requirements</span></span>



| <span data-ttu-id="3a57f-125">需求</span><span class="sxs-lookup"><span data-stu-id="3a57f-125">Requirement</span></span> | <span data-ttu-id="3a57f-126">值</span><span class="sxs-lookup"><span data-stu-id="3a57f-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a57f-127">標頭</span><span class="sxs-lookup"><span data-stu-id="3a57f-127">Header</span></span><br/> | <dl> <span data-ttu-id="3a57f-128"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a57f-128"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a57f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a57f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a57f-130">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="3a57f-130">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 





---
description: 當 DVD 瀏覽器篩選進入 [卡拉 ok] 模式時，它會透過 AM \_ 屬性 \_ DVDKARAOKE ENABLE 屬性通知音訊解碼器 \_ 。
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: 'DVD 卡拉 Dvdmedia 屬性集 (.h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2918513de06a657436ed99e67f672fe74a113b78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909066"
---
# <a name="dvd-karaoke-property-set"></a><span data-ttu-id="04d3d-103">DVD 卡拉卡拉屬性集</span><span class="sxs-lookup"><span data-stu-id="04d3d-103">DVD Karaoke Property Set</span></span>

<span data-ttu-id="04d3d-104">當 [DVD 流覽](dvd-navigator-filter.md) 器篩選進入 [卡拉 ok] 模式時，它會透過 **AM \_ 屬性 \_ DVDKARAOKE \_ ENABLE** 屬性通知音訊解碼器。</span><span class="sxs-lookup"><span data-stu-id="04d3d-104">When the [DVD Navigator](dvd-navigator-filter.md) filter goes into karaoke mode, it informs the audio decoder through the **AM\_PROPERTY\_DVDKARAOKE\_ENABLE** property.</span></span> <span data-ttu-id="04d3d-105">然後，此解碼器必須將音訊通道2到5靜音，直到它從 DVD 導覽器收到 am **\_ 屬性 \_ DVDKARAOKE \_ 資料** 屬性，並以 [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) 資料結構的指標指出如何混合輔助通道。</span><span class="sxs-lookup"><span data-stu-id="04d3d-105">The decoder should then mute audio channels 2 through 5 until it receives from the DVD Navigator an **AM\_PROPERTY\_DVDKARAOKE\_DATA** property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) data structure indicating how the auxiliary channels are to be mixed.</span></span>



| <span data-ttu-id="04d3d-106">標籤</span><span class="sxs-lookup"><span data-stu-id="04d3d-106">Label</span></span> | <span data-ttu-id="04d3d-107">值</span><span class="sxs-lookup"><span data-stu-id="04d3d-107">Value</span></span> |
|-------------------|-----------------------------|
| <span data-ttu-id="04d3d-108">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="04d3d-108">Property Set GUID</span></span> | <span data-ttu-id="04d3d-109">AM \_ KSPROPSETID \_ DvdKaraoke</span><span class="sxs-lookup"><span data-stu-id="04d3d-109">AM\_KSPROPSETID\_DvdKaraoke</span></span> |



 



| <span data-ttu-id="04d3d-110">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="04d3d-110">Property ID</span></span>                      | <span data-ttu-id="04d3d-111">描述</span><span class="sxs-lookup"><span data-stu-id="04d3d-111">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d3d-112">AM \_ 屬性 \_ DVDKARAOKE \_ 啟用</span><span class="sxs-lookup"><span data-stu-id="04d3d-112">AM\_PROPERTY\_DVDKARAOKE\_ENABLE</span></span> | <span data-ttu-id="04d3d-113">布林值。</span><span class="sxs-lookup"><span data-stu-id="04d3d-113">BOOLEAN value.</span></span> <span data-ttu-id="04d3d-114">DVD 導覽器會將 AM \_ 屬性 \_ DVDKARAOKE 啟用，並將值設為 \_ **TRUE** ，以啟用卡拉卡拉 downmixing 或 **FALSE** 來停用它。</span><span class="sxs-lookup"><span data-stu-id="04d3d-114">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_ENABLE with a value of **TRUE** to enable karaoke downmixing or **FALSE** to disable it.</span></span>                                                                                                                                    |
| <span data-ttu-id="04d3d-115">AM \_ 屬性 \_ DVDKARAOKE \_ 資料</span><span class="sxs-lookup"><span data-stu-id="04d3d-115">AM\_PROPERTY\_DVDKARAOKE\_DATA</span></span>   | <span data-ttu-id="04d3d-116">DVD 導覽器 \_ \_ 會以 \_ [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) 結構的指標傳送 DVDKARAOKE 資料屬性給解碼器，以變更 downmix 設定; 也就是，若要開啟或關閉特定的卡拉卡拉通道，並將其導向右邊或左輸出通道。</span><span class="sxs-lookup"><span data-stu-id="04d3d-116">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_DATA property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) structure to change the downmix configuration; that is, to turn certain karaoke channels on or off and direct them to the right or left output channel.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="04d3d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="04d3d-117">Requirements</span></span>



| <span data-ttu-id="04d3d-118">需求</span><span class="sxs-lookup"><span data-stu-id="04d3d-118">Requirement</span></span> | <span data-ttu-id="04d3d-119">值</span><span class="sxs-lookup"><span data-stu-id="04d3d-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04d3d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="04d3d-120">Header</span></span><br/> | <dl> <span data-ttu-id="04d3d-121"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="04d3d-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04d3d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04d3d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d3d-123">屬性集</span><span class="sxs-lookup"><span data-stu-id="04d3d-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 





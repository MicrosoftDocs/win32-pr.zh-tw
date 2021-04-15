---
description: 剪輯會 epecifies 媒體來源。
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: 剪切元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe975113f370b13e50ba695d6fb3388a43c3a74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467510"
---
# <a name="clip-element"></a><span data-ttu-id="24a1c-103">剪切元素</span><span class="sxs-lookup"><span data-stu-id="24a1c-103">clip Element</span></span>

> [!Note]  
> <span data-ttu-id="24a1c-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="24a1c-104">\[Deprecated.</span></span> <span data-ttu-id="24a1c-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="24a1c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="24a1c-106">`clip`Epecifies 媒體來源。</span><span class="sxs-lookup"><span data-stu-id="24a1c-106">The `clip` epecifies a media source.</span></span>

## <a name="attributes"></a><span data-ttu-id="24a1c-107">屬性</span><span class="sxs-lookup"><span data-stu-id="24a1c-107">Attributes</span></span>

<span data-ttu-id="24a1c-108">[**clsid**](clsid-attribute.md)、 [**畫面播放速率**](framerate-attribute.md)、 [**鎖定**](lock-attribute.md)、 [**mlength**](mlength-attribute.md)、 [**mstart**](mstart-attribute.md)、 [**mstop**](mstop-attribute.md)、 [**靜音**](mute-attribute.md)、 [**src**](src-attribute.md)、 [**start**](start-attribute.md)、 [**stop**](stop-attribute.md)、 [**stream**](stream-attribute.md)、 [**stretchmode**](stretchmode-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid**](userid-attribute.md)、 [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="24a1c-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="24a1c-109">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="24a1c-109">Parent/Child Information</span></span>



|          |                                  |
|----------|----------------------------------|
| <span data-ttu-id="24a1c-110">父代</span><span class="sxs-lookup"><span data-stu-id="24a1c-110">Parent</span></span>   | [<span data-ttu-id="24a1c-111">**跟蹤**</span><span class="sxs-lookup"><span data-stu-id="24a1c-111">**track**</span></span>](track-element.md)   |
| <span data-ttu-id="24a1c-112">Children</span><span class="sxs-lookup"><span data-stu-id="24a1c-112">Children</span></span> | [<span data-ttu-id="24a1c-113">**影響**</span><span class="sxs-lookup"><span data-stu-id="24a1c-113">**effect**</span></span>](effect-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="24a1c-114">備註</span><span class="sxs-lookup"><span data-stu-id="24a1c-114">Remarks</span></span>

<span data-ttu-id="24a1c-115">**Clsid** 屬性會指定來源篩選器的 clsid 作為來源使用。</span><span class="sxs-lookup"><span data-stu-id="24a1c-115">The **clsid** attribute specifies the CLSID of a source filter to use as the source.</span></span> <span data-ttu-id="24a1c-116">請勿在相同元素內指定 **src** 和 **clsid** 屬性 `clip` 。</span><span class="sxs-lookup"><span data-stu-id="24a1c-116">Do not specify the **src** and **clsid** attributes within the same `clip` element.</span></span>

<span data-ttu-id="24a1c-117">請至少指定 **一個開始或 mstart)  (開始** 或 ，以及 (**停止** 或 **mstop**) 的一個停止時間屬性。</span><span class="sxs-lookup"><span data-stu-id="24a1c-117">Specify at least one start-time attribute (**start** or **mstart**) and one stop-time attribute (**stop** or **mstop**).</span></span> <span data-ttu-id="24a1c-118">如果未指定其中一個啟動時間屬性，它會預設為 0 (**開始** 的時間軸開頭，或 **mstart**) 的剪輯開頭。</span><span class="sxs-lookup"><span data-stu-id="24a1c-118">If one of the start-time attributes is unspecified, it defaults to 0 (the beginning of the timeline for **start**, or the beginning of the clip for **mstart**).</span></span> <span data-ttu-id="24a1c-119">如果未指定其中一個停止時間屬性，DES 會假設正常播放速率，並據此計算未指定的停止時間。</span><span class="sxs-lookup"><span data-stu-id="24a1c-119">If one of the stop-time attributes is unspecified, DES assumes a normal playback rate and calculates the unspecified stop time accordingly.</span></span> <span data-ttu-id="24a1c-120">如果同時指定了兩個停止時間，如有需要，播放速度會比正常播放更快或更慢。</span><span class="sxs-lookup"><span data-stu-id="24a1c-120">If both stop times are specified, playback is faster or slower than normal, if necessary.</span></span>

<span data-ttu-id="24a1c-121">在下列範例中，時間軸持續時間是七秒 (**停止** 減去 **開始**) 。</span><span class="sxs-lookup"><span data-stu-id="24a1c-121">In the following example, the timeline duration is seven seconds (**stop** minus **start**).</span></span> <span data-ttu-id="24a1c-122">假設採用正常播放速率，所以 media 停止時間預設為10秒， (持續時間加上 **mstart**) 。</span><span class="sxs-lookup"><span data-stu-id="24a1c-122">Normal playback rate is assumed, so the media stop time defaults to 10 seconds (the duration plus **mstart**).</span></span>


```
<clip start="2" stop="9" mstart="3" />
```



<span data-ttu-id="24a1c-123">在下一個範例中，媒體開始時間預設為0，強制媒體持續時間為10秒。</span><span class="sxs-lookup"><span data-stu-id="24a1c-123">In the next example, the media start time defaults to 0, forcing the media duration to be 10 seconds.</span></span> <span data-ttu-id="24a1c-124">時間軸的持續時間為五秒，因此剪輯會以一般速率的兩倍播放回來。</span><span class="sxs-lookup"><span data-stu-id="24a1c-124">The timeline duration is five seconds, so the clip plays back at twice the normal rate.</span></span>


```
<clip start="5" stop="10" mstop="10" />  
```



<span data-ttu-id="24a1c-125">如果 **src** 屬性指定了靜止影像，DES 會嘗試載入一連串的靜止影像來建立動畫。</span><span class="sxs-lookup"><span data-stu-id="24a1c-125">If the **src** attribute specifies a still image, DES attempts to load a series of still images to create an animation.</span></span> <span data-ttu-id="24a1c-126">例如，如果 IMAGE001.BMP **src** 屬性，DES 會尋找 IMAGE002.BMP、IMAGE003.BMP、IMAGE004.BMP 等。</span><span class="sxs-lookup"><span data-stu-id="24a1c-126">For example, if the **src** attribute is IMAGE001.BMP, DES looks for IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, and so on.</span></span> <span data-ttu-id="24a1c-127">如果存在，則會依 **幀** 速率屬性所指定的速率，以連續的數位順序顯示。</span><span class="sxs-lookup"><span data-stu-id="24a1c-127">Assuming they exist, they are displayed in sequential numerical order, at the rate specified by the **framerate** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="24a1c-128">範例</span><span class="sxs-lookup"><span data-stu-id="24a1c-128">Examples</span></span>


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a><span data-ttu-id="24a1c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24a1c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a1c-130">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="24a1c-130">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




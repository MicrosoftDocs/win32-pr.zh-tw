---
description: 剪輯會 epecifies 媒體來源。
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: 剪切元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d937f942ba7b564e65b0e37d9c11929805287da
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908666"
---
# <a name="clip-element"></a><span data-ttu-id="dd543-103">剪切元素</span><span class="sxs-lookup"><span data-stu-id="dd543-103">clip Element</span></span>

> [!Note]  
> <span data-ttu-id="dd543-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="dd543-104">\[Deprecated.</span></span> <span data-ttu-id="dd543-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="dd543-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dd543-106">`clip`Epecifies 媒體來源。</span><span class="sxs-lookup"><span data-stu-id="dd543-106">The `clip` epecifies a media source.</span></span>

## <a name="attributes"></a><span data-ttu-id="dd543-107">屬性</span><span class="sxs-lookup"><span data-stu-id="dd543-107">Attributes</span></span>

<span data-ttu-id="dd543-108">[**clsid**](clsid-attribute.md)、 [**畫面播放速率**](framerate-attribute.md)、 [**鎖定**](lock-attribute.md)、 [**mlength**](mlength-attribute.md)、 [**mstart**](mstart-attribute.md)、 [**mstop**](mstop-attribute.md)、 [**靜音**](mute-attribute.md)、 [**src**](src-attribute.md)、 [**start**](start-attribute.md)、 [**stop**](stop-attribute.md)、 [**stream**](stream-attribute.md)、 [**stretchmode**](stretchmode-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid**](userid-attribute.md)、 [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="dd543-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="dd543-109">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="dd543-109">Parent/Child Information</span></span>



| <span data-ttu-id="dd543-110">標籤</span><span class="sxs-lookup"><span data-stu-id="dd543-110">Label</span></span> | <span data-ttu-id="dd543-111">值</span><span class="sxs-lookup"><span data-stu-id="dd543-111">Value</span></span> |
|----------|----------------------------------|
| <span data-ttu-id="dd543-112">父代</span><span class="sxs-lookup"><span data-stu-id="dd543-112">Parent</span></span>   | [<span data-ttu-id="dd543-113">**跟蹤**</span><span class="sxs-lookup"><span data-stu-id="dd543-113">**track**</span></span>](track-element.md)   |
| <span data-ttu-id="dd543-114">Children</span><span class="sxs-lookup"><span data-stu-id="dd543-114">Children</span></span> | [<span data-ttu-id="dd543-115">**影響**</span><span class="sxs-lookup"><span data-stu-id="dd543-115">**effect**</span></span>](effect-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="dd543-116">備註</span><span class="sxs-lookup"><span data-stu-id="dd543-116">Remarks</span></span>

<span data-ttu-id="dd543-117">**Clsid** 屬性會指定來源篩選器的 clsid 作為來源使用。</span><span class="sxs-lookup"><span data-stu-id="dd543-117">The **clsid** attribute specifies the CLSID of a source filter to use as the source.</span></span> <span data-ttu-id="dd543-118">請勿在相同元素內指定 **src** 和 **clsid** 屬性 `clip` 。</span><span class="sxs-lookup"><span data-stu-id="dd543-118">Do not specify the **src** and **clsid** attributes within the same `clip` element.</span></span>

<span data-ttu-id="dd543-119">請至少指定 **一個開始或 mstart)  (開始** 或 ，以及 (**停止** 或 **mstop**) 的一個停止時間屬性。</span><span class="sxs-lookup"><span data-stu-id="dd543-119">Specify at least one start-time attribute (**start** or **mstart**) and one stop-time attribute (**stop** or **mstop**).</span></span> <span data-ttu-id="dd543-120">如果未指定其中一個啟動時間屬性，它會預設為 0 (**開始** 的時間軸開頭，或 **mstart**) 的剪輯開頭。</span><span class="sxs-lookup"><span data-stu-id="dd543-120">If one of the start-time attributes is unspecified, it defaults to 0 (the beginning of the timeline for **start**, or the beginning of the clip for **mstart**).</span></span> <span data-ttu-id="dd543-121">如果未指定其中一個停止時間屬性，DES 會假設正常播放速率，並據此計算未指定的停止時間。</span><span class="sxs-lookup"><span data-stu-id="dd543-121">If one of the stop-time attributes is unspecified, DES assumes a normal playback rate and calculates the unspecified stop time accordingly.</span></span> <span data-ttu-id="dd543-122">如果同時指定了兩個停止時間，如有需要，播放速度會比正常播放更快或更慢。</span><span class="sxs-lookup"><span data-stu-id="dd543-122">If both stop times are specified, playback is faster or slower than normal, if necessary.</span></span>

<span data-ttu-id="dd543-123">在下列範例中，時間軸持續時間是七秒 (**停止** 減去 **開始**) 。</span><span class="sxs-lookup"><span data-stu-id="dd543-123">In the following example, the timeline duration is seven seconds (**stop** minus **start**).</span></span> <span data-ttu-id="dd543-124">假設採用正常播放速率，所以 media 停止時間預設為10秒， (持續時間加上 **mstart**) 。</span><span class="sxs-lookup"><span data-stu-id="dd543-124">Normal playback rate is assumed, so the media stop time defaults to 10 seconds (the duration plus **mstart**).</span></span>


```
<clip start="2" stop="9" mstart="3" />
```



<span data-ttu-id="dd543-125">在下一個範例中，媒體開始時間預設為0，強制媒體持續時間為10秒。</span><span class="sxs-lookup"><span data-stu-id="dd543-125">In the next example, the media start time defaults to 0, forcing the media duration to be 10 seconds.</span></span> <span data-ttu-id="dd543-126">時間軸的持續時間為五秒，因此剪輯會以一般速率的兩倍播放回來。</span><span class="sxs-lookup"><span data-stu-id="dd543-126">The timeline duration is five seconds, so the clip plays back at twice the normal rate.</span></span>


```
<clip start="5" stop="10" mstop="10" />  
```



<span data-ttu-id="dd543-127">如果 **src** 屬性指定了靜止影像，DES 會嘗試載入一連串的靜止影像來建立動畫。</span><span class="sxs-lookup"><span data-stu-id="dd543-127">If the **src** attribute specifies a still image, DES attempts to load a series of still images to create an animation.</span></span> <span data-ttu-id="dd543-128">例如，如果 IMAGE001.BMP **src** 屬性，DES 會尋找 IMAGE002.BMP、IMAGE003.BMP、IMAGE004.BMP 等。</span><span class="sxs-lookup"><span data-stu-id="dd543-128">For example, if the **src** attribute is IMAGE001.BMP, DES looks for IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, and so on.</span></span> <span data-ttu-id="dd543-129">如果存在，則會依 **幀** 速率屬性所指定的速率，以連續的數位順序顯示。</span><span class="sxs-lookup"><span data-stu-id="dd543-129">Assuming they exist, they are displayed in sequential numerical order, at the rate specified by the **framerate** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="dd543-130">範例</span><span class="sxs-lookup"><span data-stu-id="dd543-130">Examples</span></span>


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a><span data-ttu-id="dd543-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd543-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd543-132">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="dd543-132">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




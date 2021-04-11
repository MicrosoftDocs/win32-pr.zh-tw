---
description: 代表材質的長條圖。
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineHistogram 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FC720568-6C8E-4B14-BCB1-5FA14D32C785
api_name:
- PixEngineHistogram
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c19b77c962121949cc2495170061fee3adcecfc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109289"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span data-ttu-id="ed61f-103"><span id="vspixengine.pixenginehistogram"></span>PixEngineHistogram 結構</span><span class="sxs-lookup"><span data-stu-id="ed61f-103"><span id="vspixengine.pixenginehistogram"></span>PixEngineHistogram structure</span></span>

<span data-ttu-id="ed61f-104">代表材質的長條圖。</span><span class="sxs-lookup"><span data-stu-id="ed61f-104">Represents a histogram of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed61f-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed61f-105">Syntax</span></span>


```C++
} PixEngineHistogram;
```

## <a name="members"></a><span data-ttu-id="ed61f-106">成員</span><span class="sxs-lookup"><span data-stu-id="ed61f-106">Members</span></span>

<span data-ttu-id="ed61f-107">**horizontalMin**</span><span class="sxs-lookup"><span data-stu-id="ed61f-107">**horizontalMin**</span></span>  
<span data-ttu-id="ed61f-108">水準軸中每個 X、Y、Z 和 W 元件的最小值 (長條圖的網域) 。</span><span class="sxs-lookup"><span data-stu-id="ed61f-108">The minimum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="ed61f-109">**horizontalMax**</span><span class="sxs-lookup"><span data-stu-id="ed61f-109">**horizontalMax**</span></span>  
<span data-ttu-id="ed61f-110">水準軸中每個 X、Y、Z 和 W 元件的最大值 (長條圖的網域) 。</span><span class="sxs-lookup"><span data-stu-id="ed61f-110">The maximum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="ed61f-111">**verticalMin**</span><span class="sxs-lookup"><span data-stu-id="ed61f-111">**verticalMin**</span></span>  
<span data-ttu-id="ed61f-112">垂直軸中每個 X、Y、Z 和 W 元件的最小值 (長條圖的範圍) 。</span><span class="sxs-lookup"><span data-stu-id="ed61f-112">The minimum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="ed61f-113">**verticalMax**</span><span class="sxs-lookup"><span data-stu-id="ed61f-113">**verticalMax**</span></span>  
<span data-ttu-id="ed61f-114">垂直軸中每個 X、Y、Z 和 W 元件的最大值 (長條圖的範圍) 。</span><span class="sxs-lookup"><span data-stu-id="ed61f-114">The maximum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="ed61f-115">**dataLength**</span><span class="sxs-lookup"><span data-stu-id="ed61f-115">**dataLength**</span></span>  
<span data-ttu-id="ed61f-116">長條圖中所考慮的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="ed61f-116">The number of samples considered in the histogram.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed61f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed61f-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ed61f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ed61f-118">Header</span></span></p></td><td><span data-ttu-id="ed61f-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="ed61f-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 




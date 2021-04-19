---
title: EQUALIZERSETTINGS.nextPreset
description: NextPreset 方法會套用下一個等化器預設值。
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- EQUALIZERSETTINGS. nextPreset Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b464c0fca9b38a14a65a24185e51813e4520eee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987958"
---
# <a name="equalizersettingsnextpreset"></a><span data-ttu-id="b6afb-104">EQUALIZERSETTINGS.nextPreset</span><span class="sxs-lookup"><span data-stu-id="b6afb-104">EQUALIZERSETTINGS.nextPreset</span></span>

<span data-ttu-id="b6afb-105">**NextPreset** 方法會套用下一個等化器預設值。</span><span class="sxs-lookup"><span data-stu-id="b6afb-105">The **nextPreset** method applies the next equalizer preset.</span></span>

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a><span data-ttu-id="b6afb-106">參數</span><span class="sxs-lookup"><span data-stu-id="b6afb-106">Parameters</span></span>

<span data-ttu-id="b6afb-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b6afb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6afb-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6afb-108">Return Value</span></span>

<span data-ttu-id="b6afb-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b6afb-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6afb-110">備註</span><span class="sxs-lookup"><span data-stu-id="b6afb-110">Remarks</span></span>

<span data-ttu-id="b6afb-111">如果目前的預設值是最後一個預設值，則會將第一個預設值設為最新的。</span><span class="sxs-lookup"><span data-stu-id="b6afb-111">If the current preset is the last one available, the first preset is made current.</span></span>

## <a name="examples"></a><span data-ttu-id="b6afb-112">範例</span><span class="sxs-lookup"><span data-stu-id="b6afb-112">Examples</span></span>


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a><span data-ttu-id="b6afb-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6afb-113">Requirements</span></span>



| <span data-ttu-id="b6afb-114">需求</span><span class="sxs-lookup"><span data-stu-id="b6afb-114">Requirement</span></span> | <span data-ttu-id="b6afb-115">值</span><span class="sxs-lookup"><span data-stu-id="b6afb-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b6afb-116">版本</span><span class="sxs-lookup"><span data-stu-id="b6afb-116">Version</span></span><br/> | <span data-ttu-id="b6afb-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="b6afb-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6afb-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6afb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6afb-119">**EQUALIZERSETTINGS 元素**</span><span class="sxs-lookup"><span data-stu-id="b6afb-119">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="b6afb-120">**EQUALIZERSETTINGS.previousPreset**</span><span class="sxs-lookup"><span data-stu-id="b6afb-120">**EQUALIZERSETTINGS.previousPreset**</span></span>](equalizersettings-previouspreset.md)
</dt> </dl>

 

 






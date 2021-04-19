---
title: IWMPSettings 餘額屬性
description: 餘額屬性會取得或設定目前的立體餘額。
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- 平衡屬性 Windows Media Player
- 平衡屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，餘額屬性
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978803"
---
# <a name="iwmpsettingsbalance-property"></a><span data-ttu-id="f5999-106">IWMPSettings：：餘額屬性</span><span class="sxs-lookup"><span data-stu-id="f5999-106">IWMPSettings::balance property</span></span>

<span data-ttu-id="f5999-107">**餘額** 屬性會取得或設定目前的立體餘額。</span><span class="sxs-lookup"><span data-stu-id="f5999-107">The **balance** property gets or sets the current stereo balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5999-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5999-108">Syntax</span></span>


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="f5999-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="f5999-109">Property value</span></span>

<span data-ttu-id="f5999-110">表示餘額值的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="f5999-110">A **System.Int32** that is the balance value.</span></span> <span data-ttu-id="f5999-111">此值的範圍可以從100到100。</span><span class="sxs-lookup"><span data-stu-id="f5999-111">This value can range from  100 to 100.</span></span> <span data-ttu-id="f5999-112">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="f5999-112">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5999-113">備註</span><span class="sxs-lookup"><span data-stu-id="f5999-113">Remarks</span></span>

<span data-ttu-id="f5999-114">值為零表示音訊在左右通道的相同磁片區上播放。</span><span class="sxs-lookup"><span data-stu-id="f5999-114">The value zero indicates that the audio plays at equal volume on both left and right channels.</span></span> <span data-ttu-id="f5999-115">值為100表示音訊只會在左邊的頻道播放。</span><span class="sxs-lookup"><span data-stu-id="f5999-115">A value of  100 indicates that audio plays only on the left channel.</span></span> <span data-ttu-id="f5999-116">值為100表示音訊只會在右聲道上播放。</span><span class="sxs-lookup"><span data-stu-id="f5999-116">A value of 100 indicates that audio plays only on the right channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5999-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5999-117">Requirements</span></span>



| <span data-ttu-id="f5999-118">需求</span><span class="sxs-lookup"><span data-stu-id="f5999-118">Requirement</span></span> | <span data-ttu-id="f5999-119">值</span><span class="sxs-lookup"><span data-stu-id="f5999-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5999-120">版本</span><span class="sxs-lookup"><span data-stu-id="f5999-120">Version</span></span><br/>   | <span data-ttu-id="f5999-121">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="f5999-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="f5999-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="f5999-122">Namespace</span></span><br/> | <span data-ttu-id="f5999-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f5999-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f5999-124">組件</span><span class="sxs-lookup"><span data-stu-id="f5999-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f5999-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="f5999-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5999-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5999-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5999-127">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f5999-127">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 






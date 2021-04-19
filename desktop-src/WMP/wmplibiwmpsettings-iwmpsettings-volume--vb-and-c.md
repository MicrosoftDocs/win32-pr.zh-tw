---
title: IWMPSettings volume 屬性
description: Volume 屬性會取得或設定目前的播放磁片區。
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- 磁片區屬性 Windows Media Player
- volume 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，磁片區屬性
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992843"
---
# <a name="iwmpsettingsvolume-property"></a><span data-ttu-id="ade8a-106">IWMPSettings：： volume 屬性</span><span class="sxs-lookup"><span data-stu-id="ade8a-106">IWMPSettings::volume property</span></span>

<span data-ttu-id="ade8a-107">**Volume** 屬性會取得或設定目前的播放磁片區。</span><span class="sxs-lookup"><span data-stu-id="ade8a-107">The **volume** property gets or sets the current playback volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="ade8a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ade8a-108">Syntax</span></span>


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="ade8a-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="ade8a-109">Property value</span></span>

<span data-ttu-id="ade8a-110">為磁片區層級的 **system.object** ，範圍從0到100。</span><span class="sxs-lookup"><span data-stu-id="ade8a-110">A **System.Int32** that is the volume level, ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="ade8a-111">備註</span><span class="sxs-lookup"><span data-stu-id="ade8a-111">Remarks</span></span>

<span data-ttu-id="ade8a-112">值為零，表示沒有任何磁片區 (靜音) 。</span><span class="sxs-lookup"><span data-stu-id="ade8a-112">A value of zero specifies no volume (muted).</span></span> <span data-ttu-id="ade8a-113">值為100時，會指定完整磁片區。</span><span class="sxs-lookup"><span data-stu-id="ade8a-113">A value of 100 specifies full volume.</span></span> <span data-ttu-id="ade8a-114">如果未指定此屬性的值，則預設為針對 Windows Media Player 所建立的最後一個磁片區設定。</span><span class="sxs-lookup"><span data-stu-id="ade8a-114">If no value is specified for this property, it defaults to the last volume setting established for Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="ade8a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ade8a-115">Requirements</span></span>



| <span data-ttu-id="ade8a-116">需求</span><span class="sxs-lookup"><span data-stu-id="ade8a-116">Requirement</span></span> | <span data-ttu-id="ade8a-117">值</span><span class="sxs-lookup"><span data-stu-id="ade8a-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ade8a-118">版本</span><span class="sxs-lookup"><span data-stu-id="ade8a-118">Version</span></span><br/>   | <span data-ttu-id="ade8a-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="ade8a-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ade8a-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="ade8a-120">Namespace</span></span><br/> | <span data-ttu-id="ade8a-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ade8a-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ade8a-122">組件</span><span class="sxs-lookup"><span data-stu-id="ade8a-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ade8a-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="ade8a-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ade8a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ade8a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ade8a-125">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ade8a-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 






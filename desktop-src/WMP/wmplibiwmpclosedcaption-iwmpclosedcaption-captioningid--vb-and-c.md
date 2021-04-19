---
title: IWMPClosedCaption captioningId 屬性
description: IWMPClosedCaption 屬性會取得或設定顯示字幕的 HTML 元素名稱。
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- captioningId 屬性 Windows Media Player
- captioningId 屬性 Windows Media Player，IWMPClosedCaption 介面
- IWMPClosedCaption 介面 Windows Media Player，captioningId 屬性
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983077"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a><span data-ttu-id="56025-106">IWMPClosedCaption：： captioningId 屬性</span><span class="sxs-lookup"><span data-stu-id="56025-106">IWMPClosedCaption::captioningId property</span></span>

<span data-ttu-id="56025-107">**IWMPClosedCaption** 屬性會取得或設定顯示字幕的 HTML 元素名稱。</span><span class="sxs-lookup"><span data-stu-id="56025-107">The **IWMPClosedCaption** property gets or sets the name of the HTML element displaying the captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="56025-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="56025-108">Syntax</span></span>


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a><span data-ttu-id="56025-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="56025-109">Property value</span></span>

<span data-ttu-id="56025-110">表示 HTML 元素之識別碼的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="56025-110">The **System.String** that is the ID of the HTML element.</span></span>

## <a name="remarks"></a><span data-ttu-id="56025-111">備註</span><span class="sxs-lookup"><span data-stu-id="56025-111">Remarks</span></span>

<span data-ttu-id="56025-112">指定的元素名稱可以是網頁中的任何 HTML 專案，只要它支援 **innerHTML** 屬性即可。</span><span class="sxs-lookup"><span data-stu-id="56025-112">The element name specified can be any HTML element in the webpage as long as it supports the **innerHTML** attribute.</span></span> <span data-ttu-id="56025-113">如果網頁包含多個框架，元素名稱只能參考與 Windows Media Player 控制項相同框架中的元素。</span><span class="sxs-lookup"><span data-stu-id="56025-113">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Windows Media Player control.</span></span>

## <a name="requirements"></a><span data-ttu-id="56025-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="56025-114">Requirements</span></span>



| <span data-ttu-id="56025-115">需求</span><span class="sxs-lookup"><span data-stu-id="56025-115">Requirement</span></span> | <span data-ttu-id="56025-116">值</span><span class="sxs-lookup"><span data-stu-id="56025-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56025-117">版本</span><span class="sxs-lookup"><span data-stu-id="56025-117">Version</span></span><br/>   | <span data-ttu-id="56025-118">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="56025-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="56025-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="56025-119">Namespace</span></span><br/> | <span data-ttu-id="56025-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="56025-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="56025-121">組件</span><span class="sxs-lookup"><span data-stu-id="56025-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="56025-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="56025-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56025-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56025-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56025-124">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="56025-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="56025-125">**IWMPClosedCaption 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="56025-125">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="56025-126">**IWMPClosedCaption2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="56025-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 






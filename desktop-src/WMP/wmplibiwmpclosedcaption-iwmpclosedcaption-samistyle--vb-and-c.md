---
title: IWMPClosedCaption SAMIStyle 屬性
description: SAMIStyle 屬性會取得或設定隱藏式輔助字幕樣式。
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- SAMIStyle 屬性 Windows Media Player
- SAMIStyle 屬性 Windows Media Player，IWMPClosedCaption 介面
- IWMPClosedCaption 介面 Windows Media Player，SAMIStyle 屬性
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd0b48fc1807d6ca1854651c7f222183a845be3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984428"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a><span data-ttu-id="245d8-106">IWMPClosedCaption：： SAMIStyle 屬性</span><span class="sxs-lookup"><span data-stu-id="245d8-106">IWMPClosedCaption::SAMIStyle property</span></span>

<span data-ttu-id="245d8-107">**SAMIStyle** 屬性會取得或設定隱藏式輔助字幕樣式。</span><span class="sxs-lookup"><span data-stu-id="245d8-107">The **SAMIStyle** property gets or sets the closed captioning style.</span></span>

## <a name="syntax"></a><span data-ttu-id="245d8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="245d8-108">Syntax</span></span>


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a><span data-ttu-id="245d8-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="245d8-109">Property value</span></span>

<span data-ttu-id="245d8-110">**System.string** ，此為薩米文檔案的樣式識別碼中所指定的名稱。</span><span class="sxs-lookup"><span data-stu-id="245d8-110">The **System.String** that is the name specified in the style identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="245d8-111">備註</span><span class="sxs-lookup"><span data-stu-id="245d8-111">Remarks</span></span>

<span data-ttu-id="245d8-112">薩米文檔案可以包含數個格式樣式定義。</span><span class="sxs-lookup"><span data-stu-id="245d8-112">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="245d8-113">薩米文的樣式定義于薩米文檔案的 <STYLE> 和 </STYLE> 標記之間。</span><span class="sxs-lookup"><span data-stu-id="245d8-113">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="245d8-114">樣式的定義是以文字字串前面加上 \# 字元。</span><span class="sxs-lookup"><span data-stu-id="245d8-114">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="245d8-115">例如：</span><span class="sxs-lookup"><span data-stu-id="245d8-115">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



<span data-ttu-id="245d8-116">這會指定產生特定字型的樣式。</span><span class="sxs-lookup"><span data-stu-id="245d8-116">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="245d8-117">如果未指定薩米體樣式，預設會使用薩米文檔案中所定義的第一個樣式。</span><span class="sxs-lookup"><span data-stu-id="245d8-117">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="245d8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="245d8-118">Requirements</span></span>



| <span data-ttu-id="245d8-119">需求</span><span class="sxs-lookup"><span data-stu-id="245d8-119">Requirement</span></span> | <span data-ttu-id="245d8-120">值</span><span class="sxs-lookup"><span data-stu-id="245d8-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="245d8-121">版本</span><span class="sxs-lookup"><span data-stu-id="245d8-121">Version</span></span><br/>   | <span data-ttu-id="245d8-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="245d8-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="245d8-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="245d8-123">Namespace</span></span><br/> | <span data-ttu-id="245d8-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="245d8-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="245d8-125">組件</span><span class="sxs-lookup"><span data-stu-id="245d8-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="245d8-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="245d8-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="245d8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="245d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="245d8-128">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="245d8-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="245d8-129">**IWMPClosedCaption 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="245d8-129">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="245d8-130">**IWMPClosedCaption2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="245d8-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 






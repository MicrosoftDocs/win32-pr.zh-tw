---
title: IWMPClosedCaption SAMILang 屬性
description: SAMILang 屬性會取得或設定針對隱藏式輔助字幕所顯示的語言。
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- SAMILang 屬性 Windows Media Player
- SAMILang 屬性 Windows Media Player，IWMPClosedCaption 介面
- IWMPClosedCaption 介面 Windows Media Player，SAMILang 屬性
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997030"
---
# <a name="iwmpclosedcaptionsamilang-property"></a><span data-ttu-id="545da-106">IWMPClosedCaption：： SAMILang 屬性</span><span class="sxs-lookup"><span data-stu-id="545da-106">IWMPClosedCaption::SAMILang property</span></span>

<span data-ttu-id="545da-107">**SAMILang** 屬性會取得或設定針對隱藏式輔助字幕所顯示的語言。</span><span class="sxs-lookup"><span data-stu-id="545da-107">The **SAMILang** property gets or sets the language displayed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="545da-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="545da-108">Syntax</span></span>


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a><span data-ttu-id="545da-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="545da-109">Property value</span></span>

<span data-ttu-id="545da-110">**System.string** ，這是在薩米文檔案的語言識別項中所指定的名稱。</span><span class="sxs-lookup"><span data-stu-id="545da-110">The **System.String** that is the name specified in the language identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="545da-111">備註</span><span class="sxs-lookup"><span data-stu-id="545da-111">Remarks</span></span>

<span data-ttu-id="545da-112">薩米文檔案可以包含一或多個語言的文字。</span><span class="sxs-lookup"><span data-stu-id="545da-112">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="545da-113">隱藏式字幕的可用語言會定義于薩米文檔案的 <STYLE> 和 </STYLE> 標記之間。</span><span class="sxs-lookup"><span data-stu-id="545da-113">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="545da-114">語言識別項是使用唯一的英數位元字串所指定，該字串前面會加上句點 (。 ) 。</span><span class="sxs-lookup"><span data-stu-id="545da-114">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="545da-115">針對語言指定的名稱可以是任何字串。</span><span class="sxs-lookup"><span data-stu-id="545da-115">The name specified for a language can be any string.</span></span> <span data-ttu-id="545da-116">例如，下列程式可用來定義美式英文：</span><span class="sxs-lookup"><span data-stu-id="545da-116">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



<span data-ttu-id="545da-117">如果未指定薩米文語言，預設會使用薩米文檔案中定義的第一種語言。</span><span class="sxs-lookup"><span data-stu-id="545da-117">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="545da-118">您使用 **SAMILang** 設定的字串必須符合語言規範中的 **Name** 屬性。</span><span class="sxs-lookup"><span data-stu-id="545da-118">The string you set using **SAMILang** must match the **Name** attribute in the language specifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="545da-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="545da-119">Requirements</span></span>



| <span data-ttu-id="545da-120">需求</span><span class="sxs-lookup"><span data-stu-id="545da-120">Requirement</span></span> | <span data-ttu-id="545da-121">值</span><span class="sxs-lookup"><span data-stu-id="545da-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="545da-122">版本</span><span class="sxs-lookup"><span data-stu-id="545da-122">Version</span></span><br/>   | <span data-ttu-id="545da-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="545da-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="545da-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="545da-124">Namespace</span></span><br/> | <span data-ttu-id="545da-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="545da-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="545da-126">組件</span><span class="sxs-lookup"><span data-stu-id="545da-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="545da-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="545da-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="545da-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="545da-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="545da-129">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="545da-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="545da-130">**IWMPClosedCaption 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="545da-130">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="545da-131">**IWMPClosedCaption2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="545da-131">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 






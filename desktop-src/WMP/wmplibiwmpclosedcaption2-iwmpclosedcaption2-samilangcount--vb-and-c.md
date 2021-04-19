---
title: IWMPClosedCaption2 SAMILangCount 屬性
description: SAMILangCount 屬性會取得目前的薩米文檔案所支援的語言數目。
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- SAMILangCount 屬性 Windows Media Player
- SAMILangCount 屬性 Windows Media Player，IWMPClosedCaption2 介面
- IWMPClosedCaption2 介面 Windows Media Player，SAMILangCount 屬性
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea01357de508dea319389cd14ab85ebafe0329e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987837"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a><span data-ttu-id="83fc6-106">IWMPClosedCaption2：： SAMILangCount 屬性</span><span class="sxs-lookup"><span data-stu-id="83fc6-106">IWMPClosedCaption2::SAMILangCount property</span></span>

<span data-ttu-id="83fc6-107">**SAMILangCount** 屬性會取得目前的薩米文檔案所支援的語言數目。</span><span class="sxs-lookup"><span data-stu-id="83fc6-107">The **SAMILangCount** property gets the number of languages supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="83fc6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="83fc6-108">Syntax</span></span>


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="83fc6-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="83fc6-109">Property value</span></span>

<span data-ttu-id="83fc6-110">支援的語言數目的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="83fc6-110">A **System.Int32** that is the number of languages supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="83fc6-111">備註</span><span class="sxs-lookup"><span data-stu-id="83fc6-111">Remarks</span></span>

<span data-ttu-id="83fc6-112">除非 (AxWindowsMediaPlayer 開啟數位媒體檔案，否則此屬性會傳回0。 openState 等於 13) 。</span><span class="sxs-lookup"><span data-stu-id="83fc6-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="83fc6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="83fc6-113">Requirements</span></span>



| <span data-ttu-id="83fc6-114">需求</span><span class="sxs-lookup"><span data-stu-id="83fc6-114">Requirement</span></span> | <span data-ttu-id="83fc6-115">值</span><span class="sxs-lookup"><span data-stu-id="83fc6-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83fc6-116">版本</span><span class="sxs-lookup"><span data-stu-id="83fc6-116">Version</span></span><br/>   | <span data-ttu-id="83fc6-117">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="83fc6-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="83fc6-118">命名空間</span><span class="sxs-lookup"><span data-stu-id="83fc6-118">Namespace</span></span><br/> | <span data-ttu-id="83fc6-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="83fc6-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="83fc6-120">組件</span><span class="sxs-lookup"><span data-stu-id="83fc6-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="83fc6-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="83fc6-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83fc6-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83fc6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83fc6-123">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="83fc6-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="83fc6-124">**IWMPClosedCaption 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="83fc6-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="83fc6-125">**IWMPClosedCaption. SAMILang (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="83fc6-125">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="83fc6-126">**IWMPClosedCaption2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="83fc6-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="83fc6-127">**IWMPClosedCaption2. getSAMILangName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="83fc6-127">**IWMPClosedCaption2.getSAMILangName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 






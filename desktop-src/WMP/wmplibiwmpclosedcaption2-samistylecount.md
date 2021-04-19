---
title: IWMPClosedCaption2 SAMIStyleCount 屬性
description: SAMIStyleCount 屬性會取得目前的薩米文檔案所支援的樣式數目。
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- SAMIStyleCount 屬性 Windows Media Player
- SAMIStyleCount 屬性 Windows Media Player，IWMPClosedCaption2 介面
- IWMPClosedCaption2 介面 Windows Media Player，SAMIStyleCount 屬性
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff361b4c6d34f63e86e3d8458bff4d3308cae29f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984843"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a><span data-ttu-id="98963-106">IWMPClosedCaption2：： SAMIStyleCount 屬性</span><span class="sxs-lookup"><span data-stu-id="98963-106">IWMPClosedCaption2::SAMIStyleCount property</span></span>

<span data-ttu-id="98963-107">**SAMIStyleCount** 屬性會取得目前的薩米文檔案所支援的樣式數目。</span><span class="sxs-lookup"><span data-stu-id="98963-107">The **SAMIStyleCount** property gets the number of styles supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="98963-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="98963-108">Syntax</span></span>


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="98963-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="98963-109">Property value</span></span>

<span data-ttu-id="98963-110">是樣式數目的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="98963-110">A **System.Int32** that is the number of styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="98963-111">備註</span><span class="sxs-lookup"><span data-stu-id="98963-111">Remarks</span></span>

<span data-ttu-id="98963-112">除非 (AxWindowsMediaPlayer 開啟數位媒體檔案，否則此屬性會傳回0。 openState 等於 13) 。</span><span class="sxs-lookup"><span data-stu-id="98963-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="98963-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="98963-113">Requirements</span></span>



| <span data-ttu-id="98963-114">需求</span><span class="sxs-lookup"><span data-stu-id="98963-114">Requirement</span></span> | <span data-ttu-id="98963-115">值</span><span class="sxs-lookup"><span data-stu-id="98963-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98963-116">版本</span><span class="sxs-lookup"><span data-stu-id="98963-116">Version</span></span><br/>   | <span data-ttu-id="98963-117">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="98963-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="98963-118">命名空間</span><span class="sxs-lookup"><span data-stu-id="98963-118">Namespace</span></span><br/> | <span data-ttu-id="98963-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="98963-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="98963-120">組件</span><span class="sxs-lookup"><span data-stu-id="98963-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="98963-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="98963-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98963-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98963-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98963-123">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="98963-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="98963-124">**IWMPClosedCaption 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="98963-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98963-125">**IWMPClosedCaption. SAMIStyle (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="98963-125">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98963-126">**IWMPClosedCaption2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="98963-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98963-127">**IWMPClosedCaption2. getSAMIStyleName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="98963-127">**IWMPClosedCaption2.getSAMIStyleName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 






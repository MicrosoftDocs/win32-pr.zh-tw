---
title: 'IWMPMedia. isIdentical (VB 和 C ) '
description: IsIdentical 屬性 (\_ 在 C \ ) 的 get isIdentical 方法取得值，指出指定的媒體專案是否與目前的媒體專案相同。
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia. isIdentical (VB 和 C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996238"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a><span data-ttu-id="2b2df-104">IWMPMedia. isIdentical (VB 和 c # ) </span><span class="sxs-lookup"><span data-stu-id="2b2df-104">IWMPMedia.isIdentical (VB and C#)</span></span>

<span data-ttu-id="2b2df-105">**IsIdentical** 屬性 (c # 中的 **get \_ isIdentical** 方法 ) 取得值，指出指定的媒體專案是否與目前的媒體專案相同。</span><span class="sxs-lookup"><span data-stu-id="2b2df-105">The **isIdentical** property (the **get\_isIdentical** method in C#) gets a value indicating whether the specified media item is the same as the current one.</span></span>


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a><span data-ttu-id="2b2df-106">參數</span><span class="sxs-lookup"><span data-stu-id="2b2df-106">Parameters</span></span>

<span data-ttu-id="2b2df-107">*pIWMPMedia*</span><span class="sxs-lookup"><span data-stu-id="2b2df-107">*pIWMPMedia*</span></span>

<span data-ttu-id="2b2df-108">要與目前媒體專案比較之媒體專案的 **WMPLib IWMPMedia** 介面。</span><span class="sxs-lookup"><span data-stu-id="2b2df-108">A **WMPLib.IWMPMedia** interface to the media item to be compared with the current media item.</span></span>

## <a name="property-value"></a><span data-ttu-id="2b2df-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="2b2df-109">Property Value</span></span>

<span data-ttu-id="2b2df-110">表示兩個媒體專案是否相同的 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="2b2df-110">A **System.Boolean** value that indicates whether the two media items are identical.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b2df-111">備註</span><span class="sxs-lookup"><span data-stu-id="2b2df-111">Remarks</span></span>

<span data-ttu-id="2b2df-112">**IWMPMedia. isIdentical** 是 Visual Basic 中接受參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b2df-112">**IWMPMedia.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="2b2df-113">在 c # 中，它稱為 **IWMPMedia. get \_ isIdentical** 方法。</span><span class="sxs-lookup"><span data-stu-id="2b2df-113">In C# it is referred to as the **IWMPMedia.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="2b2df-114">範例</span><span class="sxs-lookup"><span data-stu-id="2b2df-114">Examples</span></span>

<span data-ttu-id="2b2df-115">下列範例會使用 **isIdentical** 屬性 (c # 中的 **get \_ isIdentical** 方法 ) 檢查名為 newMedia 的媒體專案是否與目前的媒體專案相同。</span><span class="sxs-lookup"><span data-stu-id="2b2df-115">The following example uses the **isIdentical** property (the **get\_isIdentical** method in C#) to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="2b2df-116">如果兩者不同，則會播放新的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="2b2df-116">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="2b2df-117">否則，目前的媒體會繼續播放不中斷的。</span><span class="sxs-lookup"><span data-stu-id="2b2df-117">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="2b2df-118">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="2b2df-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

End If
```





## <a name="requirements"></a><span data-ttu-id="2b2df-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b2df-119">Requirements</span></span>



| <span data-ttu-id="2b2df-120">需求</span><span class="sxs-lookup"><span data-stu-id="2b2df-120">Requirement</span></span> | <span data-ttu-id="2b2df-121">值</span><span class="sxs-lookup"><span data-stu-id="2b2df-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2df-122">版本</span><span class="sxs-lookup"><span data-stu-id="2b2df-122">Version</span></span><br/>   | <span data-ttu-id="2b2df-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="2b2df-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2b2df-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="2b2df-124">Namespace</span></span><br/> | <span data-ttu-id="2b2df-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2b2df-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2b2df-126">組件</span><span class="sxs-lookup"><span data-stu-id="2b2df-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2b2df-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="2b2df-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b2df-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b2df-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b2df-129">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2b2df-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






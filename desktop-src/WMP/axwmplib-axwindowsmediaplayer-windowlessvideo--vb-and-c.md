---
title: AxWindowsMediaPlayer. windowlessVideo 屬性
description: WindowlessVideo 屬性會取得或設定值，這個值表示 Windows Media Player 控制項是否以無視窗模式呈現影片。
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- windowlessVideo 屬性 Windows Media Player
- windowlessVideo 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，windowlessVideo 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996107"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a><span data-ttu-id="bd96e-106">AxWindowsMediaPlayer. windowlessVideo 屬性</span><span class="sxs-lookup"><span data-stu-id="bd96e-106">AxWindowsMediaPlayer.windowlessVideo property</span></span>

<span data-ttu-id="bd96e-107">WindowlessVideo 屬性會取得或設定值，這個值表示 Windows Media Player 控制項是否以無視窗模式呈現影片。</span><span class="sxs-lookup"><span data-stu-id="bd96e-107">The windowlessVideo property gets or sets a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd96e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd96e-108">Syntax</span></span>


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="bd96e-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="bd96e-109">Property value</span></span>

<span data-ttu-id="bd96e-110">System.string 值，指出 Windows Media Player 控制項是否以無視窗模式呈現影片。</span><span class="sxs-lookup"><span data-stu-id="bd96e-110">A System.Boolean value indicating whether the Windows Media Player control renders video in windowless mode.</span></span> <span data-ttu-id="bd96e-111">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="bd96e-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd96e-112">備註</span><span class="sxs-lookup"><span data-stu-id="bd96e-112">Remarks</span></span>

<span data-ttu-id="bd96e-113">根據預設，內嵌的 Windows Media Player 控制項會在用戶端區域內的它自己的視窗中呈現影片。</span><span class="sxs-lookup"><span data-stu-id="bd96e-113">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="bd96e-114">當 **windowlessVideo** 設定為 true 時，Windows Media Player 物件會直接在工作區中轉譯影片，因此您可以套用特殊效果或以文字將影片分層。</span><span class="sxs-lookup"><span data-stu-id="bd96e-114">When **windowlessVideo** is set to true, the Windows Media Player object renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="bd96e-115">在 Windows Vista 中，以無視窗模式轉譯影片可能會降低效能。</span><span class="sxs-lookup"><span data-stu-id="bd96e-115">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="bd96e-116">Netscape Navigator 不支援取得這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="bd96e-116">Getting a value for this property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="bd96e-117">在 Netscape Navigator 中設定這個屬性的值可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="bd96e-117">Setting a value for this property in Netscape Navigator may yield unexpected results.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd96e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd96e-118">Requirements</span></span>



| <span data-ttu-id="bd96e-119">需求</span><span class="sxs-lookup"><span data-stu-id="bd96e-119">Requirement</span></span> | <span data-ttu-id="bd96e-120">值</span><span class="sxs-lookup"><span data-stu-id="bd96e-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd96e-121">版本</span><span class="sxs-lookup"><span data-stu-id="bd96e-121">Version</span></span><br/>   | <span data-ttu-id="bd96e-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="bd96e-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="bd96e-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="bd96e-123">Namespace</span></span><br/> | <span data-ttu-id="bd96e-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="bd96e-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="bd96e-125">組件</span><span class="sxs-lookup"><span data-stu-id="bd96e-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bd96e-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="bd96e-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd96e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd96e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd96e-128">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bd96e-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






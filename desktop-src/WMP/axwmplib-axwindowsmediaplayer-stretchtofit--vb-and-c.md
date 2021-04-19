---
title: AxWindowsMediaPlayer. stretchToFit 屬性
description: StretchToFit 屬性會取得或設定值，指出當影片視窗大於影片影像的尺寸時，Windows Media Player 控制項所顯示的影片是否會自動調整大小以符合影片視窗。
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- stretchToFit 屬性 Windows Media Player
- stretchToFit 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，stretchToFit 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001107"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a><span data-ttu-id="50bbb-106">AxWindowsMediaPlayer. stretchToFit 屬性</span><span class="sxs-lookup"><span data-stu-id="50bbb-106">AxWindowsMediaPlayer.stretchToFit property</span></span>

<span data-ttu-id="50bbb-107">StretchToFit 屬性會取得或設定值，指出當影片視窗大於影片影像的尺寸時，Windows Media Player 控制項所顯示的影片是否會自動調整大小以符合影片視窗。</span><span class="sxs-lookup"><span data-stu-id="50bbb-107">The stretchToFit property gets or sets a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="50bbb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="50bbb-108">Syntax</span></span>


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="50bbb-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="50bbb-109">Property value</span></span>

<span data-ttu-id="50bbb-110">System.string 值，指出影片是否將延展以符合視窗。</span><span class="sxs-lookup"><span data-stu-id="50bbb-110">The System.Boolean value that indicates whether the video will stretch to fit the window.</span></span> <span data-ttu-id="50bbb-111">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="50bbb-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="50bbb-112">備註</span><span class="sxs-lookup"><span data-stu-id="50bbb-112">Remarks</span></span>

<span data-ttu-id="50bbb-113">當 **stretchToFit** 設定為 true 時，Windows Media Player 控制項會維持影片的原始外觀比例。</span><span class="sxs-lookup"><span data-stu-id="50bbb-113">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="50bbb-114">如果影片的長寬比與影片視窗的外觀比例不相符，則可能會在影片影像的頂端和底部或左邊和右邊出現黑色遮罩區域。</span><span class="sxs-lookup"><span data-stu-id="50bbb-114">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="50bbb-115">這個屬性只適用于內嵌在網頁中的 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="50bbb-115">This property applies to the Windows Media Player control only when it is embedded in a webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="50bbb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="50bbb-116">Requirements</span></span>



| <span data-ttu-id="50bbb-117">需求</span><span class="sxs-lookup"><span data-stu-id="50bbb-117">Requirement</span></span> | <span data-ttu-id="50bbb-118">值</span><span class="sxs-lookup"><span data-stu-id="50bbb-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50bbb-119">版本</span><span class="sxs-lookup"><span data-stu-id="50bbb-119">Version</span></span><br/>   | <span data-ttu-id="50bbb-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="50bbb-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="50bbb-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="50bbb-121">Namespace</span></span><br/> | <span data-ttu-id="50bbb-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="50bbb-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="50bbb-123">組件</span><span class="sxs-lookup"><span data-stu-id="50bbb-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="50bbb-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="50bbb-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50bbb-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50bbb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50bbb-126">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="50bbb-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






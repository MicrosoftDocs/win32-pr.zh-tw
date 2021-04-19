---
title: AxWindowsMediaPlayer. enableCoNtextMenu 屬性
description: EnableCoNtextMenu 屬性會取得或設定值，指出是否要啟用操作功能表，這會在按一下滑鼠右鍵時顯示。
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- enableCoNtextMenu 屬性 Windows Media Player
- enableCoNtextMenu 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，enableCoNtextMenu 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09c705fd45b9b994863ab4f93df1c3ae10858930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975739"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a><span data-ttu-id="6f83b-106">AxWindowsMediaPlayer. enableCoNtextMenu 屬性</span><span class="sxs-lookup"><span data-stu-id="6f83b-106">AxWindowsMediaPlayer.enableContextMenu property</span></span>

<span data-ttu-id="6f83b-107">EnableCoNtextMenu 屬性會取得或設定值，指出是否要啟用操作功能表，這會在按一下滑鼠右鍵時顯示。</span><span class="sxs-lookup"><span data-stu-id="6f83b-107">The enableContextMenu property gets or sets a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f83b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f83b-108">Syntax</span></span>


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="6f83b-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="6f83b-109">Property value</span></span>

<span data-ttu-id="6f83b-110">指出是否要啟用內容功能表的 system.string 值。</span><span class="sxs-lookup"><span data-stu-id="6f83b-110">A System.Boolean value that indicates whether to enable the context menu.</span></span> <span data-ttu-id="6f83b-111">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="6f83b-111">The default value is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f83b-112">備註</span><span class="sxs-lookup"><span data-stu-id="6f83b-112">Remarks</span></span>

<span data-ttu-id="6f83b-113">在全螢幕播放期間，Windows Media Player 會在 **enableCoNtextMenu** 等於 False 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。</span><span class="sxs-lookup"><span data-stu-id="6f83b-113">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="requirements"></a><span data-ttu-id="6f83b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f83b-114">Requirements</span></span>



| <span data-ttu-id="6f83b-115">需求</span><span class="sxs-lookup"><span data-stu-id="6f83b-115">Requirement</span></span> | <span data-ttu-id="6f83b-116">值</span><span class="sxs-lookup"><span data-stu-id="6f83b-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f83b-117">版本</span><span class="sxs-lookup"><span data-stu-id="6f83b-117">Version</span></span><br/>   | <span data-ttu-id="6f83b-118">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="6f83b-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="6f83b-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="6f83b-119">Namespace</span></span><br/> | <span data-ttu-id="6f83b-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="6f83b-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="6f83b-121">組件</span><span class="sxs-lookup"><span data-stu-id="6f83b-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6f83b-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="6f83b-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f83b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f83b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f83b-124">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6f83b-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






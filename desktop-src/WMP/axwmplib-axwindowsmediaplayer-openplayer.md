---
title: AxWindowsMediaPlayer. openPlayer 方法
description: OpenPlayer 方法會使用指定的 URL 開啟 Windows Media Player。 |AxWindowsMediaPlayer. openPlayer 方法
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- openPlayer 方法 Windows Media Player
- openPlayer 方法 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，openPlayer 方法
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998599"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a><span data-ttu-id="8ca43-107">AxWindowsMediaPlayer. openPlayer 方法</span><span class="sxs-lookup"><span data-stu-id="8ca43-107">AxWindowsMediaPlayer.openPlayer method</span></span>

<span data-ttu-id="8ca43-108">**OpenPlayer** 方法會使用指定的 URL 開啟 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="8ca43-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca43-109">語法</span><span class="sxs-lookup"><span data-stu-id="8ca43-109">Syntax</span></span>


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="8ca43-110">參數</span><span class="sxs-lookup"><span data-stu-id="8ca43-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca43-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="8ca43-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="8ca43-112">**System.string** ，此為要播放之媒體專案的 URL。</span><span class="sxs-lookup"><span data-stu-id="8ca43-112">The **System.String** that is the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca43-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ca43-113">Return value</span></span>

<span data-ttu-id="8ca43-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8ca43-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca43-115">備註</span><span class="sxs-lookup"><span data-stu-id="8ca43-115">Remarks</span></span>

<span data-ttu-id="8ca43-116">這個方法會啟動 Windows Media Player，並將指定的 URL 設定為目前的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="8ca43-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="8ca43-117">如果播放程式之前是在面板模式中關閉，則會使用使用者最後選擇的面板來開啟。</span><span class="sxs-lookup"><span data-stu-id="8ca43-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="8ca43-118">否則，播放會以完整模式開啟。</span><span class="sxs-lookup"><span data-stu-id="8ca43-118">Otherwise, the Player opens in full mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca43-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ca43-119">Requirements</span></span>



| <span data-ttu-id="8ca43-120">需求</span><span class="sxs-lookup"><span data-stu-id="8ca43-120">Requirement</span></span> | <span data-ttu-id="8ca43-121">值</span><span class="sxs-lookup"><span data-stu-id="8ca43-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca43-122">版本</span><span class="sxs-lookup"><span data-stu-id="8ca43-122">Version</span></span><br/>   | <span data-ttu-id="8ca43-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="8ca43-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="8ca43-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="8ca43-124">Namespace</span></span><br/> | <span data-ttu-id="8ca43-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="8ca43-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8ca43-126">組件</span><span class="sxs-lookup"><span data-stu-id="8ca43-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8ca43-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="8ca43-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca43-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ca43-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca43-129">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8ca43-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






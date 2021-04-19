---
title: AxWindowsMediaPlayer. close 方法
description: Close 方法會關閉目前的數位媒體檔案，在 Windows Media Player 中停止播放，並 Windows Media Player 資源釋出。
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- close 方法 Windows Media Player
- close 方法 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，close 方法
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981120"
---
# <a name="axwindowsmediaplayerclose-method"></a><span data-ttu-id="826a9-106">AxWindowsMediaPlayer. close 方法</span><span class="sxs-lookup"><span data-stu-id="826a9-106">AxWindowsMediaPlayer.close method</span></span>

<span data-ttu-id="826a9-107">Close 方法會關閉目前的數位媒體檔案，在 Windows Media Player 中停止播放，並 Windows Media Player 資源釋出。</span><span class="sxs-lookup"><span data-stu-id="826a9-107">The close method closes the current digital media file, stops playback in Windows Media Player and releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="826a9-108">語法</span><span class="sxs-lookup"><span data-stu-id="826a9-108">Syntax</span></span>


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a><span data-ttu-id="826a9-109">參數</span><span class="sxs-lookup"><span data-stu-id="826a9-109">Parameters</span></span>

<span data-ttu-id="826a9-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="826a9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="826a9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="826a9-111">Return value</span></span>

<span data-ttu-id="826a9-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="826a9-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="826a9-113">備註</span><span class="sxs-lookup"><span data-stu-id="826a9-113">Remarks</span></span>

<span data-ttu-id="826a9-114">這個方法會關閉目前的數位媒體檔案，而不是 Windows Media Player 本身。</span><span class="sxs-lookup"><span data-stu-id="826a9-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="826a9-115">範例</span><span class="sxs-lookup"><span data-stu-id="826a9-115">Examples</span></span>

<span data-ttu-id="826a9-116">下列範例會建立一個按鈕，當按下此按鈕時，會在 Windows Media Player 中停止播放，並釋放使用中的資源。</span><span class="sxs-lookup"><span data-stu-id="826a9-116">The following example creates a button that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="826a9-117">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="826a9-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="826a9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="826a9-118">Requirements</span></span>



| <span data-ttu-id="826a9-119">需求</span><span class="sxs-lookup"><span data-stu-id="826a9-119">Requirement</span></span> | <span data-ttu-id="826a9-120">值</span><span class="sxs-lookup"><span data-stu-id="826a9-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="826a9-121">版本</span><span class="sxs-lookup"><span data-stu-id="826a9-121">Version</span></span><br/>   | <span data-ttu-id="826a9-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="826a9-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="826a9-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="826a9-123">Namespace</span></span><br/> | <span data-ttu-id="826a9-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="826a9-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="826a9-125">組件</span><span class="sxs-lookup"><span data-stu-id="826a9-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="826a9-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="826a9-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="826a9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="826a9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826a9-128">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="826a9-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






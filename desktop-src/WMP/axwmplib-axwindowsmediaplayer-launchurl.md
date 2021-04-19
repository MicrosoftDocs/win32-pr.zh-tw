---
title: AxWindowsMediaPlayer. launchURL 方法
description: LaunchURL 方法會將 URL 傳送給使用者的預設瀏覽器，以呈現。 |AxWindowsMediaPlayer. launchURL 方法
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- launchURL 方法 Windows Media Player
- launchURL 方法 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，launchURL 方法
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27fe8e544bb14b119785b26b9cb5be5cdad48015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990789"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a><span data-ttu-id="baf5f-107">AxWindowsMediaPlayer. launchURL 方法</span><span class="sxs-lookup"><span data-stu-id="baf5f-107">AxWindowsMediaPlayer.launchURL method</span></span>

<span data-ttu-id="baf5f-108">LaunchURL 方法會將 URL 傳送給使用者的預設瀏覽器，以呈現。</span><span class="sxs-lookup"><span data-stu-id="baf5f-108">The launchURL method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="baf5f-109">語法</span><span class="sxs-lookup"><span data-stu-id="baf5f-109">Syntax</span></span>


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="baf5f-110">參數</span><span class="sxs-lookup"><span data-stu-id="baf5f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baf5f-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="baf5f-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="baf5f-112">要啟動之 URL 的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="baf5f-112">The **System.String** that is the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baf5f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="baf5f-113">Return value</span></span>

<span data-ttu-id="baf5f-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="baf5f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="baf5f-115">備註</span><span class="sxs-lookup"><span data-stu-id="baf5f-115">Remarks</span></span>

<span data-ttu-id="baf5f-116">這個方法只會使用 HTTP 或 HTTPS 通訊協定來開啟網頁。</span><span class="sxs-lookup"><span data-stu-id="baf5f-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

## <a name="examples"></a><span data-ttu-id="baf5f-117">範例</span><span class="sxs-lookup"><span data-stu-id="baf5f-117">Examples</span></span>

<span data-ttu-id="baf5f-118">下列範例會建立一個按鈕，當您按一下此按鈕時，就會在新的瀏覽器視窗中顯示 Microsoft 網站。</span><span class="sxs-lookup"><span data-stu-id="baf5f-118">The following example creates a button that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="baf5f-119">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="baf5f-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="baf5f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="baf5f-120">Requirements</span></span>



| <span data-ttu-id="baf5f-121">需求</span><span class="sxs-lookup"><span data-stu-id="baf5f-121">Requirement</span></span> | <span data-ttu-id="baf5f-122">值</span><span class="sxs-lookup"><span data-stu-id="baf5f-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baf5f-123">版本</span><span class="sxs-lookup"><span data-stu-id="baf5f-123">Version</span></span><br/>   | <span data-ttu-id="baf5f-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="baf5f-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="baf5f-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="baf5f-125">Namespace</span></span><br/> | <span data-ttu-id="baf5f-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="baf5f-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="baf5f-127">組件</span><span class="sxs-lookup"><span data-stu-id="baf5f-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="baf5f-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="baf5f-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baf5f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="baf5f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baf5f-130">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="baf5f-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






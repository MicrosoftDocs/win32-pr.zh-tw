---
title: AxWindowsMediaPlayer. URL 屬性
description: URL 屬性會取得或設定要播放之媒體專案的名稱。
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- URL 屬性 Windows Media Player
- URL 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，URL 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ed9e601aa581e988bac1a233f06c4f5c552353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995986"
---
# <a name="axwindowsmediaplayerurl-property"></a><span data-ttu-id="4a158-106">AxWindowsMediaPlayer. URL 屬性</span><span class="sxs-lookup"><span data-stu-id="4a158-106">AxWindowsMediaPlayer.URL property</span></span>

<span data-ttu-id="4a158-107">URL 屬性會取得或設定要播放之媒體專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a158-107">The URL property gets or sets the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a158-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a158-108">Syntax</span></span>


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a><span data-ttu-id="4a158-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="4a158-109">Property value</span></span>

<span data-ttu-id="4a158-110">System.string，此為媒體專案的 URL。</span><span class="sxs-lookup"><span data-stu-id="4a158-110">A System.String that is the URL of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a158-111">備註</span><span class="sxs-lookup"><span data-stu-id="4a158-111">Remarks</span></span>

<span data-ttu-id="4a158-112">這個屬性只能設定為安全性區域中的 URL，該 URL 的安全性區域與呼叫的程式或網頁的安全性區域相同或較不嚴格。</span><span class="sxs-lookup"><span data-stu-id="4a158-112">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="4a158-113">如果使用功能變數名稱伺服器 (DNS) 名稱（而非 IP 位址）指定位址，則從防火牆後方開啟媒體專案的應用程式將會有較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="4a158-113">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="4a158-114">請勿從事件處理常式程式碼呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="4a158-114">Do not call this method from event handler code.</span></span> <span data-ttu-id="4a158-115">從事件處理常式呼叫 **URL** 可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="4a158-115">Calling **URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="4a158-116">範例</span><span class="sxs-lookup"><span data-stu-id="4a158-116">Examples</span></span>

<span data-ttu-id="4a158-117">下列範例可讓使用者在文字方塊中輸入檔案路徑，以指定媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="4a158-117">The following example allows the user to specify a media file by entering a file path in a text box.</span></span> <span data-ttu-id="4a158-118">按一下按鈕時，[URL] 屬性會設定為指定的檔案，並播放該檔案。</span><span class="sxs-lookup"><span data-stu-id="4a158-118">When a button is clicked, the URL property is set to the specified file and the file is played.</span></span> <span data-ttu-id="4a158-119">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="4a158-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4a158-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a158-120">Requirements</span></span>



| <span data-ttu-id="4a158-121">需求</span><span class="sxs-lookup"><span data-stu-id="4a158-121">Requirement</span></span> | <span data-ttu-id="4a158-122">值</span><span class="sxs-lookup"><span data-stu-id="4a158-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a158-123">版本</span><span class="sxs-lookup"><span data-stu-id="4a158-123">Version</span></span><br/>   | <span data-ttu-id="4a158-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="4a158-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4a158-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="4a158-125">Namespace</span></span><br/> | <span data-ttu-id="4a158-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4a158-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4a158-127">組件</span><span class="sxs-lookup"><span data-stu-id="4a158-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4a158-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="4a158-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a158-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a158-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a158-130">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4a158-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






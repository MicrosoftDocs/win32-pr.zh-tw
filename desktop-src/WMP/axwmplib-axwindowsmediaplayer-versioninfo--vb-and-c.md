---
title: AxWindowsMediaPlayer. versionInfo 屬性
description: VersionInfo 屬性會取得值，這個值會指定 Windows Media Player 的版本。
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- versionInfo 屬性 Windows Media Player
- versionInfo 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，versionInfo 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f759c2aedb19e21c4b7d90f3634141e4c37ec8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995985"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a><span data-ttu-id="09b59-106">AxWindowsMediaPlayer. versionInfo 屬性</span><span class="sxs-lookup"><span data-stu-id="09b59-106">AxWindowsMediaPlayer.versionInfo property</span></span>

<span data-ttu-id="09b59-107">VersionInfo 屬性會取得值，這個值會指定 Windows Media Player 的版本。</span><span class="sxs-lookup"><span data-stu-id="09b59-107">The versionInfo property gets a value that specifies the version of the Windows Media Player.</span></span>

<span data-ttu-id="09b59-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="09b59-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b59-109">語法</span><span class="sxs-lookup"><span data-stu-id="09b59-109">Syntax</span></span>


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a><span data-ttu-id="09b59-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="09b59-110">Property value</span></span>

<span data-ttu-id="09b59-111">以下列格式表示版本資訊的 System.string *： "0.0.\*\*Yyyy*」，其中 *X* 代表主要版本號碼，而 *yyyy* 代表組建編號。</span><span class="sxs-lookup"><span data-stu-id="09b59-111">A System.String that is the version information in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="09b59-112">範例</span><span class="sxs-lookup"><span data-stu-id="09b59-112">Examples</span></span>

<span data-ttu-id="09b59-113">下列範例會建立一個按鈕，當按下此按鈕時，就會顯示訊息方塊，其中包含 Windows Media Player 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="09b59-113">The following example creates a button that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="09b59-114">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="09b59-114">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="09b59-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="09b59-115">Requirements</span></span>



| <span data-ttu-id="09b59-116">需求</span><span class="sxs-lookup"><span data-stu-id="09b59-116">Requirement</span></span> | <span data-ttu-id="09b59-117">值</span><span class="sxs-lookup"><span data-stu-id="09b59-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09b59-118">版本</span><span class="sxs-lookup"><span data-stu-id="09b59-118">Version</span></span><br/>   | <span data-ttu-id="09b59-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="09b59-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="09b59-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="09b59-120">Namespace</span></span><br/> | <span data-ttu-id="09b59-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="09b59-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="09b59-122">組件</span><span class="sxs-lookup"><span data-stu-id="09b59-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="09b59-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="09b59-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09b59-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09b59-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09b59-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="09b59-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






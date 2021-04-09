---
title: 參考 Url 中的外觀
description: 參考 Url 中的外觀
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Windows Media Player 的外觀、URL 參考
- 外觀、URL 參考
- 外觀中的 URL 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675564"
---
# <a name="referencing-skins-in-urls"></a><span data-ttu-id="78c65-106">參考 Url 中的外觀</span><span class="sxs-lookup"><span data-stu-id="78c65-106">Referencing Skins in URLs</span></span>

<span data-ttu-id="78c65-107">如果您使用 URL 載入將由 Windows Media Player 播放的媒體檔案，您可以要求使用特定的外觀搭配該檔案。</span><span class="sxs-lookup"><span data-stu-id="78c65-107">If you use a URL to load a media file that will be played by Windows Media Player, you can request that a particular skin be used with that file.</span></span> <span data-ttu-id="78c65-108">如果已在使用者的電腦上安裝該面板，則會使用該面板;否則，將會使用先前的外觀。</span><span class="sxs-lookup"><span data-stu-id="78c65-108">If the skin is already installed on the user's machine, it will be used; otherwise the previous skin will be used.</span></span>

<span data-ttu-id="78c65-109">若要要求面板，請將下列內容新增至 URL 的結尾：</span><span class="sxs-lookup"><span data-stu-id="78c65-109">To request a skin, add the following to the end of the URL:</span></span>


```C++
?WMPSkin=skinname
```



<span data-ttu-id="78c65-110">*skinname* 是您想要要求的面板名稱。</span><span class="sxs-lookup"><span data-stu-id="78c65-110">*skinname* is the name of the skin you want to request.</span></span> <span data-ttu-id="78c65-111">請勿在面板的名稱前後使用引號。</span><span class="sxs-lookup"><span data-stu-id="78c65-111">Do not use quotes around the name of the skin.</span></span>

<span data-ttu-id="78c65-112">例如，若要要求使用 headspace 面板，請輸入下列 HTTP URL：</span><span class="sxs-lookup"><span data-stu-id="78c65-112">For example, to request the headspace skin be used, type the following http URL:</span></span>


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a><span data-ttu-id="78c65-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="78c65-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78c65-114">**關於外觀**</span><span class="sxs-lookup"><span data-stu-id="78c65-114">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 





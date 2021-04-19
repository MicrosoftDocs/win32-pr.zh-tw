---
title: Co-Branding 線上商店
description: Co-Branding 線上商店
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player 線上商店、共同品牌
- 線上商店、共同品牌
- 輸入1個線上商店、共同品牌
- 輸入2個線上商店、共同品牌
- 共同品牌的線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969855"
---
# <a name="co-branding-online-stores"></a><span data-ttu-id="e850b-108">Co-Branding 線上商店</span><span class="sxs-lookup"><span data-stu-id="e850b-108">Co-Branding Online Stores</span></span>

<span data-ttu-id="e850b-109">未操作音樂商店的個人電腦 Oem 可以與線上商店提供者共同品牌。</span><span class="sxs-lookup"><span data-stu-id="e850b-109">Personal computer OEMs who do not operate a music store can co-brand with online store providers.</span></span> <span data-ttu-id="e850b-110">Windows Media Player 安裝程式支援 ServiceExtra 命令列參數，可讓硬體 Oem 設定線上商店可用來識別安裝初始線上商店的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="e850b-110">Windows Media Player setup supports the ServiceExtra command line parameter to enable hardware OEMs to set a custom attribute that the online store can use to identify which OEM installed the initial online store.</span></span>

<span data-ttu-id="e850b-111">例如，如果名為 Fabrikam 的電腦製作者想要將初始線上商店設定為 Proseware 音樂存放區，它可能會使用下列命令列來安裝 Windows Media Player 10：</span><span class="sxs-lookup"><span data-stu-id="e850b-111">For example, if a computer maker named Fabrikam wants to set the initial online store to the Proseware music store, it might use the following command line to install Windows Media Player 10:</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



<span data-ttu-id="e850b-112">以這種方式安裝 Windows Media Player 時，播放程式會在每次開啟 Proseware 服務時附加 ServiceExtra 字串。</span><span class="sxs-lookup"><span data-stu-id="e850b-112">When Windows Media Player is installed in this manner, the Player appends the ServiceExtra string each time it opens the Proseware service.</span></span> <span data-ttu-id="e850b-113">下列範例顯示 Windows Media Player 會傳送至 Proseware 服務以取得 ServiceInfo 檔的 URL：</span><span class="sxs-lookup"><span data-stu-id="e850b-113">The following example shows the URL that Windows Media Player would send to the Proseware service to retrieve the ServiceInfo document:</span></span>


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



<span data-ttu-id="e850b-114">Proseware online store 接著可以使用查詢字串來判斷 Windows Media Player 安裝的 OEM，並傳回動態產生的 ServiceInfo 檔，指向線上商店的共同品牌版本。</span><span class="sxs-lookup"><span data-stu-id="e850b-114">The Proseware online store can then use the query string to determine which OEM installed Windows Media Player and return a dynamically generated ServiceInfo document that points to the co-branded version of the online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e850b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="e850b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e850b-116">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="e850b-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e850b-117">**安裝線上商店的命令列參數**</span><span class="sxs-lookup"><span data-stu-id="e850b-117">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 





---
description: 安裝資料庫或轉換中的關鍵字摘要屬性包含關鍵字清單。
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: 關鍵字摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3828146fef861cd993331045d6a1380d84c2bbc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990922"
---
# <a name="keywords-summary-property"></a><span data-ttu-id="ed18d-103">關鍵字摘要屬性</span><span class="sxs-lookup"><span data-stu-id="ed18d-103">Keywords Summary property</span></span>

<span data-ttu-id="ed18d-104">安裝資料庫或轉換中的 **關鍵字摘要** 屬性包含關鍵字清單。</span><span class="sxs-lookup"><span data-stu-id="ed18d-104">The **Keywords Summary** property in installation databases or transforms contains a list of keywords.</span></span> <span data-ttu-id="ed18d-105">檔案瀏覽器可以使用關鍵字來搜尋檔案的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="ed18d-105">The keywords may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="ed18d-106">此屬性包含修補程式套件中修補程式來源的清單。</span><span class="sxs-lookup"><span data-stu-id="ed18d-106">This property contains a list of sources of the patch in a patch package.</span></span>

<span data-ttu-id="ed18d-107">它是由安裝資料庫、轉換或修補套件的作者所組成，以提供摘要資訊中這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="ed18d-107">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="ed18d-108">作者應該執行下列動作，以判斷正確的值。</span><span class="sxs-lookup"><span data-stu-id="ed18d-108">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="ed18d-109">在安裝套件中，將這個屬性的值設定為關鍵字清單。</span><span class="sxs-lookup"><span data-stu-id="ed18d-109">In an installation package, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="ed18d-110">關鍵字應包含「安裝程式」和產品特定關鍵字，而且可能會進行當地語系化。</span><span class="sxs-lookup"><span data-stu-id="ed18d-110">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="ed18d-111">在轉換中，將這個屬性的值設定為關鍵字清單。</span><span class="sxs-lookup"><span data-stu-id="ed18d-111">In a transform, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="ed18d-112">關鍵字應包含「安裝程式」和產品特定關鍵字，而且可能會進行當地語系化。</span><span class="sxs-lookup"><span data-stu-id="ed18d-112">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="ed18d-113">在修補程式套件中，將這個屬性的值設定為修補程式來源的網路或 URL 位置清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="ed18d-113">In a patch package, set the value of this property to a semicolon-delimited list of network or URL locations for the sources of the patch.</span></span> <span data-ttu-id="ed18d-114">安裝修補程式之後，安裝程式會將這些修補程式新增至修補套件的來源清單。</span><span class="sxs-lookup"><span data-stu-id="ed18d-114">When the patch is installed, the installer adds these to the source list for the patch package.</span></span> <span data-ttu-id="ed18d-115">如果快取的 patch 遺失，安裝程式就可以在原始位置中搜尋來源、 **關鍵字摘要** 屬性加入來源清單中的位置，或是使用 [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) 或 [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) 函式新增至來源清單的位置。</span><span class="sxs-lookup"><span data-stu-id="ed18d-115">If the cached patch becomes missing, the installer can search for a source in the original location, a location added to the source list by the **Keywords Summary** property, or a location added to the source list using the [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) or [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed18d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed18d-116">Requirements</span></span>



| <span data-ttu-id="ed18d-117">需求</span><span class="sxs-lookup"><span data-stu-id="ed18d-117">Requirement</span></span> | <span data-ttu-id="ed18d-118">值</span><span class="sxs-lookup"><span data-stu-id="ed18d-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed18d-119">版本</span><span class="sxs-lookup"><span data-stu-id="ed18d-119">Version</span></span><br/> | <span data-ttu-id="ed18d-120">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="ed18d-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ed18d-121">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="ed18d-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ed18d-122">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ed18d-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed18d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed18d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed18d-124">摘要屬性描述</span><span class="sxs-lookup"><span data-stu-id="ed18d-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 





---
title: 從 Web Pages 呼叫 WDS
description: 您可以使用瀏覽器協助程式物件，從您建立或維護的任何網頁，呼叫 Microsoft Windows 桌面搜尋 (WDS)  (BHO) 和 Windows Internet Explorer。
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2020
ms.locfileid: "104023148"
---
# <a name="calling-wds-from-web-pages"></a><span data-ttu-id="78436-103">從 Web Pages 呼叫 WDS</span><span class="sxs-lookup"><span data-stu-id="78436-103">Calling WDS from Web Pages</span></span>

> [!NOTE]
> <span data-ttu-id="78436-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="78436-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="78436-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="78436-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="78436-106">您可以使用瀏覽器協助程式物件，從您建立或維護的任何網頁，呼叫 Microsoft Windows 桌面搜尋 (WDS)  (BHO) 和 Windows Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="78436-106">You can call Microsoft Windows Desktop Search (WDS) from any webpage you create or maintain using the Browser Helper Object (BHO) and Windows Internet Explorer.</span></span> <span data-ttu-id="78436-107">您可以在 MSN 網頁上查看其運作方式。</span><span class="sxs-lookup"><span data-stu-id="78436-107">You can see how this works on the MSN webpage.</span></span> <span data-ttu-id="78436-108">在上的搜尋方塊上方 https://www.msn.com 有數種搜尋類型： Web、新聞、影像、桌面、百科全書和 Local。</span><span class="sxs-lookup"><span data-stu-id="78436-108">Above the search box on https://www.msn.com are several search types: Web, News, Images, Desktop, Encarta, and Local.</span></span> <span data-ttu-id="78436-109">如果您按一下 [桌面]，會將搜尋參數傳遞至 Windows 桌面搜尋，以搜尋目錄並在 WDS 使用者介面中顯示結果。</span><span class="sxs-lookup"><span data-stu-id="78436-109">If you click Desktop, the search parameters are passed to Windows Desktop Search, which searches the catalog and displays results in the WDS user interface.</span></span> <span data-ttu-id="78436-110">若要讓使用者從您的網頁 (s) 啟動桌面搜尋，必須在其系統上安裝並啟用 WDSBHO、您的網頁 (s) 必須以 WDS 註冊為允許的 URL，而且您必須建立連結以將使用者 enetered 查詢傳遞至 WDS。</span><span class="sxs-lookup"><span data-stu-id="78436-110">For users to start a desktop search from your webpage(s), the WDSBHO must be installed and enabled on their systems, your webpage(s) must be registered with WDS as an allowed URL, and you must create a link to pass the user-enetered query to WDS.</span></span>

## <a name="enabling-the-wds-browser-help-object"></a><span data-ttu-id="78436-111">啟用 WDS 瀏覽器說明物件</span><span class="sxs-lookup"><span data-stu-id="78436-111">Enabling the WDS Browser Help Object</span></span>

<span data-ttu-id="78436-112">當您安裝 WDS 時，預設會在 Internet Explorer 中安裝並啟用 BHO，但您可以輕鬆地確認它尚未停用或卸載。</span><span class="sxs-lookup"><span data-stu-id="78436-112">The BHO is installed and enabled within Internet Explorer by default when you install WDS, but you can easily verify that it hasn't been disabled or uninstalled.</span></span> <span data-ttu-id="78436-113">在使用者的系統上，開啟 Internet Explorer，從 [**工具**] 功能表中選取 [**網際網路選項**]，按一下 [**程式**] 索引標籤，然後按一下 [**管理附加** 元件]。</span><span class="sxs-lookup"><span data-stu-id="78436-113">On a user's system, open Internet Explorer , select **Internet Options** from the **Tools** menu, click the **Programs** tab, and then click **Manage Add-Ons**.</span></span> <span data-ttu-id="78436-114">在附加元件清單中，尋找 dsWebAllowBHO 類別，並確定已啟用。</span><span class="sxs-lookup"><span data-stu-id="78436-114">In your list of add-ons, look for the dsWebAllowBHO Class and make sure it is enabled.</span></span> <span data-ttu-id="78436-115">停用 BHO 時，WDS 將繼續正常運作;不過，您將無法從網頁搜尋桌面。</span><span class="sxs-lookup"><span data-stu-id="78436-115">When the BHO is disabled, WDS will continue to work normally; however, you will not be able to search the desktop from a webpage.</span></span>

<span data-ttu-id="78436-116">以下兩個允許桌面搜尋的選項都將使用已註冊的搜尋應用程式，在本機執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="78436-116">Both of the following options for allowing a desktop search will execute the search locally with the registered search application.</span></span>

## <a name="registering-web-page-urls"></a><span data-ttu-id="78436-117">註冊網頁 Url</span><span class="sxs-lookup"><span data-stu-id="78436-117">Registering Web Page URLs</span></span>

<span data-ttu-id="78436-118">登錄包含可從中呼叫 WDS 的「允許」網域 Url 清單。</span><span class="sxs-lookup"><span data-stu-id="78436-118">The Registry includes a list of "allowed" domain URLs from which WDS can be called.</span></span> <span data-ttu-id="78436-119">若要將您的網頁 (的) ，您必須在登錄中列出您的網域 URL (s) 為 REG SZ，如下所示 \_ ：</span><span class="sxs-lookup"><span data-stu-id="78436-119">To include your webpage(s), you need to list your domain URL(s) as REG\_SZ in the Registry as follows:</span></span>

<span data-ttu-id="78436-120">**HKEY \_允許本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows 桌面搜尋** \\ **DSW** \\ \\*<number>* = <domainURL></span><span class="sxs-lookup"><span data-stu-id="78436-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows Desktop Search**\\**DSW**\\**Allowed**\\*<number>* = <domainURL></span></span>

<span data-ttu-id="78436-121">其中 **<number>** 是依序編號，而 **<domainURL>** 是您想要允許 WDS 搜尋的網頁 URL。</span><span class="sxs-lookup"><span data-stu-id="78436-121">Where **<number>** is sequentially numbered, and **<domainURL>** is the URL of the Web Page you want to allow WDS searches from.</span></span> <span data-ttu-id="78436-122">此 URL 字串可以 \* 在 URL 的開頭或結尾包含萬用字元星號。</span><span class="sxs-lookup"><span data-stu-id="78436-122">This URL string can include the wildcard asterisk \* at the beginning or end of the URL.</span></span> <span data-ttu-id="78436-123">例如，如果字串為 " \* . mydomain.com"，則您可以從和啟動 WDS 搜尋 https://www.mydomain.com https://mydomain.com 。</span><span class="sxs-lookup"><span data-stu-id="78436-123">For example, if the string is "\*.mydomain.com", then you can start a WDS search from both https://www.mydomain.com and https://mydomain.com.</span></span>

## <a name="enabling-desktop-search-by-url"></a><span data-ttu-id="78436-124">依 URL 啟用桌面搜尋</span><span class="sxs-lookup"><span data-stu-id="78436-124">Enabling Desktop Search by URL</span></span>

<span data-ttu-id="78436-125">另一個不需要存取登錄的選項是在網頁上使用下列 URL (s) ：</span><span class="sxs-lookup"><span data-stu-id="78436-125">Another option that does not require access to the Registry is to use the following URL on your webpage(s):</span></span>

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

<span data-ttu-id="78436-126">其中 **QUERY** 是使用者正在搜尋的 URL 編碼字串，包括任何 [先進的查詢語法](-search-2x-wds-aqsreference.md) 字詞。</span><span class="sxs-lookup"><span data-stu-id="78436-126">where **QUERY** is the URL-encoded string the user is searching on, including any [Advanced Query Syntax](-search-2x-wds-aqsreference.md) terms.</span></span>

 

 





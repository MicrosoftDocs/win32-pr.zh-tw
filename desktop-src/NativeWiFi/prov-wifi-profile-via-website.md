---
title: 透過網站佈建 Wi-Fi 設定檔
description: 允許您的使用者從網站下載設定檔，並布建。
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933586"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a><span data-ttu-id="694c0-103">透過網站佈建 Wi-Fi 設定檔</span><span class="sxs-lookup"><span data-stu-id="694c0-103">Provision a Wi-Fi profile via a website</span></span>

<span data-ttu-id="694c0-104">本主題所述的工作流程是在 Windows 10 2004 版中引進。</span><span class="sxs-lookup"><span data-stu-id="694c0-104">The workflow described in this topic was introduced in Windows 10, version 2004.</span></span> <span data-ttu-id="694c0-105">本主題說明如何設定網站，讓使用者可以布建 Passpoint 網路的設定檔 (或一般網路) ，再移至對應的 Wi-Fi 存取點的範圍。</span><span class="sxs-lookup"><span data-stu-id="694c0-105">This topic shows how to configure a website so that a user can provision a profile for a Passpoint network (or for a normal network) prior to moving into range of the corresponding Wi-Fi access points.</span></span> <span data-ttu-id="694c0-106">其中一個範例案例是，可能打算首次造訪機場或會議的使用者，並且想要在家裡下載和布建設定檔以事先準備。</span><span class="sxs-lookup"><span data-stu-id="694c0-106">An example scenario is that of a user who might be planning to visit an airport or a conference for the first time, and they want to prepare in advance by downloading and provisioning a profile at home.</span></span>

<span data-ttu-id="694c0-107">作為開發人員，您可以藉由提供 XML 設定檔和設定網站來啟用工作流程。</span><span class="sxs-lookup"><span data-stu-id="694c0-107">As a developer, you enable the workflow by providing an XML profile, and configuring a website.</span></span> <span data-ttu-id="694c0-108">然後，您的使用者就可以透過網頁瀏覽器從您的網站下載 Wi-Fi 設定檔。</span><span class="sxs-lookup"><span data-stu-id="694c0-108">Your users can then provision a Wi-Fi profile by downloading it from your website via a web browser.</span></span> <span data-ttu-id="694c0-109">在使用者的裝置上，接著會使用 [URI 啟用] 和 [Windows **設定** ] 應用程式來布建 Wi-Fi 設定檔。</span><span class="sxs-lookup"><span data-stu-id="694c0-109">On the user's device, the Wi-Fi profile is then provisioned by using URI activation and the Windows **Settings** app.</span></span>

<span data-ttu-id="694c0-110">此工作流程會取代 Internet Explorer 中用於布建 Wi-Fi 設定檔的機制，而這些設定檔依賴 Microsoft 特定的 JavaScript Api。</span><span class="sxs-lookup"><span data-stu-id="694c0-110">This workflow supersedes the mechanism in Internet Explorer for provisioning Wi-Fi profiles, which relies on Microsoft-specific JavaScript APIs.</span></span> <span data-ttu-id="694c0-111">這項新的工作流程預期會與所有主要瀏覽器搭配運作。</span><span class="sxs-lookup"><span data-stu-id="694c0-111">This new workflow is expected to work with all major browsers.</span></span>

## <a name="the-workflow-in-more-detail"></a><span data-ttu-id="694c0-112">更詳細的工作流程</span><span class="sxs-lookup"><span data-stu-id="694c0-112">The workflow in more detail</span></span>

<span data-ttu-id="694c0-113">您可以從包含做為引數的超連結啟動此工作流程，以提供 XML 檔的下載 URI。</span><span class="sxs-lookup"><span data-stu-id="694c0-113">You can activate this workflow from a hyperlink that includes as an argument the download URI of the provisioning XML document.</span></span>

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

<span data-ttu-id="694c0-114">例如，下列 HTML 標籤會提供一個連結，以安裝在假設檔中找到的設定檔 (s) `http://contoso.com/ProvisioningDoc.xml` 。</span><span class="sxs-lookup"><span data-stu-id="694c0-114">For example, the following HTML markup gives a link to install the profile(s) that are found in a hypothetical document `http://contoso.com/ProvisioningDoc.xml`.</span></span>

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

<span data-ttu-id="694c0-115">您的 XML 必須遵守布建架構 (查看 [帳戶](/windows-hardware/drivers/mobilebroadband/account-provisioning) 布建) 。</span><span class="sxs-lookup"><span data-stu-id="694c0-115">Your XML must adhere to the provisioning schema (see [Account provisioning](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span></span> <span data-ttu-id="694c0-116">您的 XML 也必須包含一或多個 [WLANProfile](./wlan-profileschema-wlanprofile-element.md)   元素。</span><span class="sxs-lookup"><span data-stu-id="694c0-116">Your XML must also include one or more [WLANProfile](./wlan-profileschema-wlanprofile-element.md) elements.</span></span><span data-ttu-id="694c0-117">每個設定檔會顯示在 [ **新增** ] 對話方塊中，如下所述。</span><span class="sxs-lookup"><span data-stu-id="694c0-117"> Each profile will be displayed in the **Add** dialog described next.</span></span>

<span data-ttu-id="694c0-118">當使用者按一下您的 HTML 連結時，會在 [ **設定** ] 應用程式中叫用安裝工作流程。</span><span class="sxs-lookup"><span data-stu-id="694c0-118">When the user clicks your HTML link, the installation workflow is invoked in the **Settings** app.</span></span> <span data-ttu-id="694c0-119">[ **設定** ] 應用程式會下載您的布建 XML 檔。</span><span class="sxs-lookup"><span data-stu-id="694c0-119">Your provisioning XML document is downloaded by the **Settings** app.</span></span> <span data-ttu-id="694c0-120">下載後，會顯示有關設定檔、簽章和簽署者的資訊， (前提是檔遵守架構) 。</span><span class="sxs-lookup"><span data-stu-id="694c0-120">Once it's downloaded, information about the profiles, signature, and signer are displayed (provided that the document adheres to the schema).</span></span>

![設定應用程式](images/install-dialog.png)

<span data-ttu-id="694c0-122">只有當布建檔案已簽署且受信任時，才會啟用 [**設定**] 應用程式對話方塊中的 [**新增**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="694c0-122">The **Add** button in the dialog in the **Settings** app is enabled only if the provisioning file is signed and trusted.</span></span>

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a><span data-ttu-id="694c0-123">在您的網頁中，判斷是否支援此工作流程</span><span class="sxs-lookup"><span data-stu-id="694c0-123">In your web page, determine whether this workflow is supported</span></span>

<span data-ttu-id="694c0-124">在 JavaScript 中，沒有任何方法可判斷 Windows 的確切組建版本。</span><span class="sxs-lookup"><span data-stu-id="694c0-124">There is no way in JavaScript to determine the exact build version of Windows.</span></span> <span data-ttu-id="694c0-125">但是，如果您的使用者使用 Microsoft Edge 的網頁瀏覽器，您就可以檢查 HTTP 標頭的值來判斷 Edge 的版本 `User-agent` 。</span><span class="sxs-lookup"><span data-stu-id="694c0-125">But if your user is using the Microsoft Edge web browser, then you can determine the version of Edge by inspecting the value of the `User-agent` HTTP header.</span></span> <span data-ttu-id="694c0-126">如果版本大於或等於 `18.nnnnn` ，則支援工作流程。</span><span class="sxs-lookup"><span data-stu-id="694c0-126">If the version is greater than or equal to `18.nnnnn`, then the workflow is supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="694c0-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="694c0-127">Related topics</span></span>

* [<span data-ttu-id="694c0-128">帳戶布建</span><span class="sxs-lookup"><span data-stu-id="694c0-128">Account provisioning</span></span>](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [<span data-ttu-id="694c0-129">WLANProfile 元素</span><span class="sxs-lookup"><span data-stu-id="694c0-129">WLANProfile element</span></span>](./wlan-profileschema-wlanprofile-element.md)
---
title: 簡報
description: 簡報是 UPnP 流程中的最後一個步驟。
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195399316882de71c148f2369dd2978c4cfbd728
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839843"
---
# <a name="presentation"></a><span data-ttu-id="f53e2-103">簡報</span><span class="sxs-lookup"><span data-stu-id="f53e2-103">Presentation</span></span>

<span data-ttu-id="f53e2-104">簡報是 UPnP 流程中的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="f53e2-104">Presentation is the final step in the UPnP process.</span></span> <span data-ttu-id="f53e2-105">如果裝置有用於表示的 URL，則控制點可以從此 URL 取出頁面，並將頁面載入瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="f53e2-105">If a device has a URL for presentation, a control point can retrieve a page from this URL and load the page into a browser.</span></span> <span data-ttu-id="f53e2-106">視簡報頁面和裝置的功能而定，控制點可以控制裝置並查看裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="f53e2-106">Depending on the capabilities of the presentation page and the device, the control point can control the device and view the status of the device.</span></span>

<span data-ttu-id="f53e2-107">在註冊期間傳遞給 [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) 的資源路徑，是所有與裝置呈現相關的檔案所在的位置。</span><span class="sxs-lookup"><span data-stu-id="f53e2-107">The resource path, which is passed to [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) during registration, is where all the files relevant to the presentation of the device are located.</span></span> <span data-ttu-id="f53e2-108">裝置開發人員可以為每個內嵌裝置提供個別頁面。</span><span class="sxs-lookup"><span data-stu-id="f53e2-108">Device developers can provide separate pages for each embedded device.</span></span> <span data-ttu-id="f53e2-109">裝置描述範本中的表示 URL 可以是絕對 URL 或相對 URL。</span><span class="sxs-lookup"><span data-stu-id="f53e2-109">The presentation URL in the device description template can either be an absolute URL or a relative URL.</span></span> <span data-ttu-id="f53e2-110">針對相對於資源路徑的相對 Url，裝置描述範本應該包含檔案名。</span><span class="sxs-lookup"><span data-stu-id="f53e2-110">For relative URLs, which are relative to the resource path, the device description template should contain a file name.</span></span> <span data-ttu-id="f53e2-111">**IUPnPRegistrar** 會將此值轉換為實際位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="f53e2-111">**IUPnPRegistrar** converts this to a URL with the actual location.</span></span> <span data-ttu-id="f53e2-112">若為絕對 Url，則不會修改位置。</span><span class="sxs-lookup"><span data-stu-id="f53e2-112">For absolute URLs, the location is not modified.</span></span>

<span data-ttu-id="f53e2-113">為了在簡報頁面內支援用戶端腳本，額外的資訊通常會以「查詢字串」的形式附加至 URL。</span><span class="sxs-lookup"><span data-stu-id="f53e2-113">To support client side scripts within a presentation page, extra information is normally appended to the URL in the form of a "query string".</span></span> <span data-ttu-id="f53e2-114">附加的額外資訊是裝置描述檔的 URL，以及裝置或內嵌裝置的 UDN。</span><span class="sxs-lookup"><span data-stu-id="f53e2-114">The extra information that is appended is the URL to the device description document, and the UDN of the device or embedded device.</span></span> <span data-ttu-id="f53e2-115">裝置描述 URL 可以用來在腳本中載入描述檔，然後透過其服務控制裝置。</span><span class="sxs-lookup"><span data-stu-id="f53e2-115">The device description URL can be used to load a description document in the script, and then control the device through its services.</span></span> <span data-ttu-id="f53e2-116">UDN 用來從根裝置選取內嵌裝置。</span><span class="sxs-lookup"><span data-stu-id="f53e2-116">The UDN is used to select an embedded device from the root device.</span></span>

<span data-ttu-id="f53e2-117">修改過之呈現 URL 的格式為：實際的簡報 URL，問號 ( "？") ，裝置描述 URL、加號 ( "+" ) 、裝置 UDN。</span><span class="sxs-lookup"><span data-stu-id="f53e2-117">The format of the modified presentation URL is: the actual presentation URL, a question mark ("?"), the device description URL, a plus sign ("+"), the device UDN.</span></span> <span data-ttu-id="f53e2-118">問號代表查詢字串的開頭。</span><span class="sxs-lookup"><span data-stu-id="f53e2-118">The question mark denotes the start of the query string.</span></span>

<span data-ttu-id="f53e2-119">如果裝置描述範本中的簡報 URL 是絕對 URL，而且它已包含問號 ( "？") ，則不會將額外的資訊新增至展示 URL。</span><span class="sxs-lookup"><span data-stu-id="f53e2-119">If the presentation URL in the device description template was an absolute URL and it already contained a question mark ("?"), then the extra information is not added to the presentation URL.</span></span>



| <span data-ttu-id="f53e2-120">描述</span><span class="sxs-lookup"><span data-stu-id="f53e2-120">Description</span></span>                        | <span data-ttu-id="f53e2-121">URL</span><span class="sxs-lookup"><span data-stu-id="f53e2-121">URL</span></span>                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f53e2-122">在裝置描述範本中</span><span class="sxs-lookup"><span data-stu-id="f53e2-122">In the device description template</span></span> | <span data-ttu-id="f53e2-123">**presentationURL** MyDevice.html **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="f53e2-123">**presentationURL** MyDevice.html **/presentationURL**</span></span>                                                                                              |
| <span data-ttu-id="f53e2-124">由裝置主機產生</span><span class="sxs-lookup"><span data-stu-id="f53e2-124">Generated by the device host</span></span>       | <span data-ttu-id="f53e2-125">**presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394...</span><span class="sxs-lookup"><span data-stu-id="f53e2-125">**presentationURL**https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394…</span></span> <span data-ttu-id="f53e2-126">+ UDN **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="f53e2-126">+ UDN **/presentationURL**</span></span> |



 

<span data-ttu-id="f53e2-127">用戶端腳本可能必須從展示 URL 中解壓縮裝置描述 URL 以載入 [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) 物件。</span><span class="sxs-lookup"><span data-stu-id="f53e2-127">A client-side script may have to extract the device description URL from the presentation URL to load the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) object.</span></span> <span data-ttu-id="f53e2-128">這是藉由取得查詢字串，並以加號 ( "+" ) 來終止。</span><span class="sxs-lookup"><span data-stu-id="f53e2-128">This is done by taking the query string, and terminating it at the plus sign ("+").</span></span>


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



<span data-ttu-id="f53e2-129">如果是內嵌裝置的簡報頁面，則需要一些額外的工作。</span><span class="sxs-lookup"><span data-stu-id="f53e2-129">In the case of a presentation page for an embedded device, some additional work is required.</span></span> <span data-ttu-id="f53e2-130">載入 [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)之後，腳本必須取得內嵌裝置的集合，然後選取符合查詢字串中 UDN 的裝置。</span><span class="sxs-lookup"><span data-stu-id="f53e2-130">After loading the [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), the script must obtain the collection of embedded devices, then select the device that matches the UDN in the query string.</span></span> <span data-ttu-id="f53e2-131">下列腳本示範如何針對目前的簡報頁面選取內嵌裝置。</span><span class="sxs-lookup"><span data-stu-id="f53e2-131">The following script shows how to select the embedded device for the current presentation page.</span></span> <span data-ttu-id="f53e2-132">它會假設已載入 LightDesc。</span><span class="sxs-lookup"><span data-stu-id="f53e2-132">It assumes LightDesc is already loaded.</span></span>


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 





---
title: 在線上時從 Web 安裝
description: 在線上時從 Web 安裝
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player 線上商店，在線上從 Web 安裝
- 線上商店，在線上從 Web 安裝
- 輸入1個線上商店，線上時從 Web 安裝
- 輸入2個線上商店，線上時從 Web 安裝
- Windows Media Player 線上商店，從 Web 安裝線上
- 線上商店，從 Web 安裝線上
- 輸入1個線上商店，從 Web 安裝線上
- 輸入2個線上商店，從 Web 安裝線上
- 在線上從 Web 安裝線上商店
- 線上商店的線上安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967627"
---
# <a name="installing-from-the-web-while-online"></a><span data-ttu-id="deb1f-113">在線上時從 Web 安裝</span><span class="sxs-lookup"><span data-stu-id="deb1f-113">Installing from the Web While Online</span></span>

<span data-ttu-id="deb1f-114">使用者可以在連線到網際網路時，將 Windows Media Player 安裝為 Web 下載。</span><span class="sxs-lookup"><span data-stu-id="deb1f-114">Users can install Windows Media Player as a Web download while connected to the Internet.</span></span> <span data-ttu-id="deb1f-115">在此情況下，Microsoft 可以設定您指定的初始線上商店。</span><span class="sxs-lookup"><span data-stu-id="deb1f-115">In this case, Microsoft can configure the initial online store that you specify.</span></span>

<span data-ttu-id="deb1f-116">若要以這種方式轉散發 Windows Media Player，請使用下列 URL：</span><span class="sxs-lookup"><span data-stu-id="deb1f-116">To redistribute Windows Media Player in this manner, use the following URL:</span></span>

<span data-ttu-id="deb1f-117"> https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*版本*&UserLocale =*localID*&Service =*key*</span><span class="sxs-lookup"><span data-stu-id="deb1f-117">https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale=*localID*&Service=*key*</span></span>

<span data-ttu-id="deb1f-118">在上述 URL 中，將 *金鑰* 設定為線上商店的金鑰名稱，並將 *localeID* 設定為存放區提供服務的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="deb1f-118">In the preceding URL, set *key* to the key name for your online store, and set *localeID* to the identifier of the locale where your store provides service.</span></span> <span data-ttu-id="deb1f-119">在 Windows XP 上將 Windows Media Player 11 的 *版本* 設定為2，或針對 Windows Media Player 10 設定為1。</span><span class="sxs-lookup"><span data-stu-id="deb1f-119">Set *version* to 2 for Windows Media Player 11 on Windows XP or 1 for Windows Media Player 10.</span></span> <span data-ttu-id="deb1f-120">此 URL 會安裝 Windows Media Player，並將初始使用中的存放區設定為索引 *鍵* 所指定的存放區。</span><span class="sxs-lookup"><span data-stu-id="deb1f-120">The URL installs Windows Media Player and sets the initial active store to the one specified by *key*.</span></span>

<span data-ttu-id="deb1f-121">下列範例會顯示安裝 Windows Media Player 11 的 URL，並將 Proseware 設定為初始使用中存放區。</span><span class="sxs-lookup"><span data-stu-id="deb1f-121">The following example shows a URL that installs Windows Media Player 11 and sets Proseware as the initial active store.</span></span> <span data-ttu-id="deb1f-122">適用于 *localeID* 的409值表示 Proseware 提供美國的服務。</span><span class="sxs-lookup"><span data-stu-id="deb1f-122">The value of 409 for *localeID* indicates that Proseware provides service in the United States.</span></span>

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

<span data-ttu-id="deb1f-123">如果線上商店的 ServiceInfo 檔包含 Install 元素，Windows Media Player 安裝程式將會自訂安裝程式。</span><span class="sxs-lookup"><span data-stu-id="deb1f-123">If the ServiceInfo document for the online store includes an Install element, Windows Media Player setup will customize the setup process.</span></span> <span data-ttu-id="deb1f-124">安裝程式會使用屬性值， (EULA) 和您的隱私權聲明中顯示您的使用者授權合約，也會將您的 .cab 檔案取出並安裝到使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="deb1f-124">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="deb1f-125">例如，您可以使用這項功能來安裝您的線上商店所需的最新 COM 物件版本。</span><span class="sxs-lookup"><span data-stu-id="deb1f-125">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="deb1f-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="deb1f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="deb1f-127">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="deb1f-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="deb1f-128">**Install 元素**</span><span class="sxs-lookup"><span data-stu-id="deb1f-128">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="deb1f-129">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="deb1f-129">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="deb1f-130">**設定初始線上商店**</span><span class="sxs-lookup"><span data-stu-id="deb1f-130">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 





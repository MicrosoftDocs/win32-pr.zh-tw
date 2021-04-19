---
description: 任何 COM + 應用程式都可以公開為 XML web service。
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: 建立 XML Web Service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997470"
---
# <a name="creating-xml-web-services"></a><span data-ttu-id="ca18b-103">建立 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="ca18b-103">Creating XML Web Services</span></span>

<span data-ttu-id="ca18b-104">任何 COM + 應用程式都可以公開為 XML web service。</span><span class="sxs-lookup"><span data-stu-id="ca18b-104">Any COM+ application can be exposed as an XML web service.</span></span> <span data-ttu-id="ca18b-105">然後，您可以從遠端呼叫應用程式在伺服器 COM +) 目錄中所設定元件 (元件的預設介面中的方法。</span><span class="sxs-lookup"><span data-stu-id="ca18b-105">The methods in the default interfaces of the applications configured components (components in the servers COM+ catalog) can then be called remotely.</span></span> <span data-ttu-id="ca18b-106">您可以使用 [元件服務] 系統管理工具來建立 IIS 虛擬根目錄，以使用 SOAP 來呼叫元件方法。</span><span class="sxs-lookup"><span data-stu-id="ca18b-106">You can use the Component Services administrative tool to create an IIS virtual root directory from which the component methods can be called by using SOAP.</span></span>

> [!Note]  
> <span data-ttu-id="ca18b-107">您必須在電腦上安裝 .NET Framework，才能將 COM + 應用程式公開為 XML web service。</span><span class="sxs-lookup"><span data-stu-id="ca18b-107">The .NET Framework must be installed on your computer in order to expose a COM+ application as an XML web service.</span></span>

 

<span data-ttu-id="ca18b-108">**將 COM + 應用程式公開為 XML web service**</span><span class="sxs-lookup"><span data-stu-id="ca18b-108">**To expose a COM+ application as an XML web service**</span></span>

1.  <span data-ttu-id="ca18b-109">在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="ca18b-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="ca18b-110">以滑鼠右鍵按一下您想要公開為 XML web service 的應用程式，然後選擇 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="ca18b-110">Right-click the application you want to expose as an XML web service, and choose **Properties**.</span></span>

3.  <span data-ttu-id="ca18b-111">按一下 [屬性] 對話方塊中的 [ **啟用** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="ca18b-111">Click the **Activation** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="ca18b-112">選取 [ **使用 SOAP** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="ca18b-112">Select the **Uses SOAP** check box.</span></span>

5.  <span data-ttu-id="ca18b-113">在 [ **SOAP VRoot** ] 文字方塊中，輸入可從遠端存取元件方法的 IIS 虛擬根目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca18b-113">In the **SOAP VRoot** text box, enter the name of the IIS virtual root directory from which the components methods can be accessed remotely.</span></span> <span data-ttu-id="ca18b-114">請注意，SOAP VRoot 不能是另一個 SOAP VRoot 目錄的子目錄。</span><span class="sxs-lookup"><span data-stu-id="ca18b-114">Note that a SOAP VRoot cannot be a subdirectory of another SOAP VRoot directory.</span></span>

6.  <span data-ttu-id="ca18b-115">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="ca18b-115">Click **OK**.</span></span>

    <span data-ttu-id="ca18b-116">如果您將 IIS 虛擬根目錄指定為 *vroot* ，且您的伺服器完整功能變數名稱為 *servername*，則您的元件會公開為 XML web service 的 URL 為 HTTPs://*servername* / *vroot*/。</span><span class="sxs-lookup"><span data-stu-id="ca18b-116">If you specify the IIS virtual root directory as *vroot* and if your servers fully qualified domain name is *servername*, the URL where your component is exposed as an XML web service is https://*servername*/*vroot*/.</span></span>

    <span data-ttu-id="ca18b-117">您檔案系統中的對應目錄是 \\ windows \\ system32 \\ com \\ SoapVRoots \\ *vroot* \\ ;COM + 會將數個設定檔和 ASP.NET 程式放在那裡。</span><span class="sxs-lookup"><span data-stu-id="ca18b-117">The corresponding directory in your file system is \\windows\\system32\\com\\SoapVRoots\\*vroot*\\; COM+ places several configuration files and ASP.NET programs there.</span></span> <span data-ttu-id="ca18b-118">若是負載過重的 XML web service，您可能會想要調整儲存在檔案 web.config 中的參數。如需此檔案的詳細資訊，請參閱 IIS 檔。</span><span class="sxs-lookup"><span data-stu-id="ca18b-118">For an XML web service under heavy load, you may want to adjust the parameters stored in the file web.config. For information about this file, consult the IIS documentation.</span></span>

    <span data-ttu-id="ca18b-119">公開為 XML web service 之 COM + 應用程式的預設安全性設定，會根據安裝的 .NET Framework 版本而有所不同。</span><span class="sxs-lookup"><span data-stu-id="ca18b-119">The default security settings for a COM+ application exposed as an XML web service differ depending on which version of the .NET Framework is installed.</span></span> <span data-ttu-id="ca18b-120">如果已安裝1.0 版，則根據預設，XML web service 不是安全的;接受所有呼叫，且不使用加密。</span><span class="sxs-lookup"><span data-stu-id="ca18b-120">If version 1.0 is installed, XML web services are nonsecure by default; all calls are accepted and no encryption is used.</span></span> <span data-ttu-id="ca18b-121">如果已安裝1.1 版或更新版本，則根據預設，XML web service 是安全的;呼叫端必須經過驗證，而且需要加密。</span><span class="sxs-lookup"><span data-stu-id="ca18b-121">If version 1.1 or later is installed, XML web services are secure by default; callers must be authenticated and encryption is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca18b-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca18b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca18b-123">以 CAO 模式存取 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="ca18b-123">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="ca18b-124">在 WKO 模式中存取 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="ca18b-124">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="ca18b-125">COM + SOAP 服務總覽</span><span class="sxs-lookup"><span data-stu-id="ca18b-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="ca18b-126">保護 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="ca18b-126">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 




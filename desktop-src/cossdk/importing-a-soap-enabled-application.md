---
description: 當啟用 SOAP 的應用程式從 proxy 模式中的伺服器匯出時，匯入該應用程式的用戶端就可以自動存取它所包含之元件的方法（從遠端），如同用戶端啟始物件中伺服器提供的 web 服務一樣 (CAO) 模式。 這可讓您輕鬆地在網路上將 COM + 應用程式的功能部署為 XML web service。
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: 匯入 SOAP-Enabled 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9faca91a726caea765d4b2ca227ddba0ff3a2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510711"
---
# <a name="importing-a-soap-enabled-application"></a><span data-ttu-id="cdbaf-104">匯入 SOAP-Enabled 應用程式</span><span class="sxs-lookup"><span data-stu-id="cdbaf-104">Importing a SOAP-Enabled Application</span></span>

<span data-ttu-id="cdbaf-105">當啟用 SOAP 的應用程式從 proxy 模式中的伺服器 [匯出](exporting-a-soap-enabled-application.md) 時，匯入該應用程式的用戶端就可以自動存取它所包含之元件的方法（從遠端），如同用戶端啟始物件中伺服器提供的 web 服務一樣 (CAO) 模式。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-105">When a SOAP-enabled application has been [exported](exporting-a-soap-enabled-application.md) from a server in proxy mode, clients that import it can automatically access the methods of the components it contains, remotely, as web services offered by the server in client-activated object (CAO) mode.</span></span> <span data-ttu-id="cdbaf-106">這可讓您輕鬆地在網路上將 COM + 應用程式的功能部署為 XML web service。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-106">This allows you to very easily deploy the functionality of a COM+ application across a network as an XML web service.</span></span>

<span data-ttu-id="cdbaf-107">在用戶端上使用以這種方式匯入之應用程式的元件時，不會在用戶端上執行，而是會使用匯出應用程式的來源伺服器所提供的 XML web service，從遠端存取。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-107">When the components of an application imported in this way are used on the client, they do not run on the client but instead are accessed remotely by using the XML web service provided by the server from which the application was exported.</span></span> <span data-ttu-id="cdbaf-108">如需使用以這種方式匯入之應用程式元件的詳細資訊，請參閱 [以 CAO 模式存取 XML Web Service](accessing-xml-web-services-in-cao-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-108">For details on using the components of an application imported in this way, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="cdbaf-109">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="cdbaf-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="cdbaf-110">若要將啟用 SOAP 的應用程式匯入至用戶端，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="cdbaf-110">To import a SOAP-enabled application into a client, use the following steps:</span></span>

1.  <span data-ttu-id="cdbaf-111">在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要安裝應用程式之用戶端電腦相關聯的資料夾。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the folder associated with the client computer on which you want to install the application.</span></span>

2.  <span data-ttu-id="cdbaf-112">在用戶端的 [ **Com + 應用程式** ] 資料夾上按一下滑鼠右鍵，然後選擇 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-112">Right-click the client's **COM+ Applications** folder, and then choose **New**.</span></span> <span data-ttu-id="cdbaf-113">**Com + 應用程式安裝精靈** 隨即出現。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-113">The **COM+ Application Install Wizard** appears.</span></span>

3.  <span data-ttu-id="cdbaf-114">在 [ **Com + 應用程式安裝] 嚮導** 中，按一下 [ **安裝預先建立的應用程式 (s])**。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-114">In the **COM+ Application Install Wizard**, click **Install pre-built application(s)**.</span></span>

4.  <span data-ttu-id="cdbaf-115">流覽網路以找出或指定您要安裝應用程式之伺服器上的 MSI 檔案的網路路徑。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-115">Browse the network to locate or specify the network path of the MSI file on the server from which you want to install the application.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="cdbaf-116">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cdbaf-116">Visual Basic</span></span>

<span data-ttu-id="cdbaf-117">不適用。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-117">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="cdbaf-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="cdbaf-118">C/C++</span></span>

<span data-ttu-id="cdbaf-119">不適用。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-119">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdbaf-120">備註</span><span class="sxs-lookup"><span data-stu-id="cdbaf-120">Remarks</span></span>

<span data-ttu-id="cdbaf-121">COM 元件是由 GUID 所識別，如果重新編譯元件，則會變更。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-121">COM components are identified by a GUID, which changes if the components are recompiled.</span></span> <span data-ttu-id="cdbaf-122">如果已重新編譯公開為 XML web service 的已設定 COM 元件，使用它的用戶端應用程式將會中斷。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-122">If a configured COM component that is exposed as an XML web service is recompiled, client applications that use it will break.</span></span> <span data-ttu-id="cdbaf-123">因此，當重新編譯公開為 XML web service 的元件時，用戶端應該重新匯入使用該元件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cdbaf-123">Therefore, when a component that is exposed as an XML web service is recompiled, clients should re-import the applications that use the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdbaf-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="cdbaf-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdbaf-125">COM + SOAP 服務總覽</span><span class="sxs-lookup"><span data-stu-id="cdbaf-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="cdbaf-126">建立 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="cdbaf-126">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="cdbaf-127">匯出 SOAP-Enabled 應用程式</span><span class="sxs-lookup"><span data-stu-id="cdbaf-127">Exporting a SOAP-Enabled Application</span></span>](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 




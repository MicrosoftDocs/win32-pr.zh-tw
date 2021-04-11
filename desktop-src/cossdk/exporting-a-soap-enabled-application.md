---
description: 當您使用 COM + 來建立 XML web service 時，該服務可供任何授權用戶端使用，包括未使用 COM + 或甚至 Microsoft Windows 的用戶端。
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: 匯出 SOAP-Enabled 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c92029f431fc06964f233c5746c283821d11c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847418"
---
# <a name="exporting-a-soap-enabled-application"></a><span data-ttu-id="a295f-103">匯出 SOAP-Enabled 應用程式</span><span class="sxs-lookup"><span data-stu-id="a295f-103">Exporting a SOAP-Enabled Application</span></span>

<span data-ttu-id="a295f-104">當您使用 COM + 來建立 XML web service 時，該服務可供任何授權用戶端使用，包括未使用 COM + 或甚至 Microsoft Windows 的用戶端。</span><span class="sxs-lookup"><span data-stu-id="a295f-104">When you use COM+ to create an XML web service, that service can be used by any authorized client, including those not using COM+ or even Microsoft Windows.</span></span> <span data-ttu-id="a295f-105">不過，在用戶端啟動的物件中使用 COM + web 服務，從 COM + 用戶端應用程式 (CAO) 模式是特別簡單的。</span><span class="sxs-lookup"><span data-stu-id="a295f-105">However, using a COM+ web service in client-activated object (CAO) mode from a COM+ client application is especially easy.</span></span> <span data-ttu-id="a295f-106">只要以 proxy 模式匯出啟用 SOAP 的應用程式，然後將它匯 [入](importing-a-soap-enabled-application.md) 您要存取對應之 XML web service 的用戶端。</span><span class="sxs-lookup"><span data-stu-id="a295f-106">Just export the SOAP-enabled application in proxy mode, and then [import](importing-a-soap-enabled-application.md) it into the client for which you want to access the corresponding XML web service.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="a295f-107">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="a295f-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="a295f-108">若要從伺服器匯出啟用 SOAP 的應用程式，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="a295f-108">To export a SOAP-enabled application from a server, use the following steps:</span></span>

1.  <span data-ttu-id="a295f-109">在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="a295f-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="a295f-110">以滑鼠右鍵按一下您想要公開為 XML web service 的元件，然後選擇 [ **匯出**]。</span><span class="sxs-lookup"><span data-stu-id="a295f-110">Right-click the component you want to expose as an XML web service, and choose **Export**.</span></span> <span data-ttu-id="a295f-111">**Com + 應用程式匯出 Wizard** 隨即出現。</span><span class="sxs-lookup"><span data-stu-id="a295f-111">The **COM+ Application Export Wizard** appears.</span></span>

3.  <span data-ttu-id="a295f-112">在標示為 **要建立之應用程式檔的完整路徑和檔案名** 的文字方塊中，輸入將包含所匯出應用程式之 MSI 檔案的完整路徑和檔案名，或按一下 **[流覽]** 以使用對話方塊來選取完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="a295f-112">In the text box labeled **Enter the full path and filename for the application file to be created**, enter the full path and filename for the MSI file that will contain the exported application, or click **Browse** to select the full path and filename using a dialog box.</span></span>

4.  <span data-ttu-id="a295f-113">在 [ **匯出為**] 下，選取 [ **應用程式 Proxy –安裝在其他電腦上，以啟用此電腦的存取** ] 選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="a295f-113">Under **Export As**, select the **Application Proxy – Install on other machines to enable access to this machine** radio button.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="a295f-114">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a295f-114">Visual Basic</span></span>

<span data-ttu-id="a295f-115">不適用。</span><span class="sxs-lookup"><span data-stu-id="a295f-115">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="a295f-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="a295f-116">C/C++</span></span>

<span data-ttu-id="a295f-117">不適用。</span><span class="sxs-lookup"><span data-stu-id="a295f-117">Does not apply.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a295f-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="a295f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a295f-119">COM + SOAP 服務總覽</span><span class="sxs-lookup"><span data-stu-id="a295f-119">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="a295f-120">建立 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="a295f-120">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="a295f-121">匯入 SOAP-Enabled 應用程式</span><span class="sxs-lookup"><span data-stu-id="a295f-121">Importing a SOAP-Enabled Application</span></span>](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 




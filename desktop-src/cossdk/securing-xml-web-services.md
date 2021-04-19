---
description: 公開為 XML web service 的 COM + 應用程式的存取權，是由處理傳入要求的 IIS web 伺服器所控制。
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: 保護 XML Web Service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94953ce0769c44ddaeda27cacdac99ab4ff252d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971145"
---
# <a name="securing-xml-web-services"></a><span data-ttu-id="19320-103">保護 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="19320-103">Securing XML Web Services</span></span>

<span data-ttu-id="19320-104">公開為 XML web service 的 COM + 應用程式的存取權，是由處理傳入要求的 IIS web 伺服器所控制。</span><span class="sxs-lookup"><span data-stu-id="19320-104">Access to COM+ applications exposed as XML web services is controlled by the IIS web server, which processes the incoming requests.</span></span> <span data-ttu-id="19320-105">您也可以將 IIS 設定為要求與呼叫端進行通訊，以透過使用安全通訊端層 (SSL) 通訊協定建立的安全通道進行通訊。</span><span class="sxs-lookup"><span data-stu-id="19320-105">You can also configure IIS to require the communications with the caller take place over a secure channel established using the Secure Sockets Layer (SSL) protocol.</span></span>

> [!Note]  
> <span data-ttu-id="19320-106">受保護的 XML web service 不支援透過 WSDL 的 WKO 存取。</span><span class="sxs-lookup"><span data-stu-id="19320-106">A secured XML web service does not support WKO access via WSDL.</span></span> <span data-ttu-id="19320-107">相反地，安裝 .NET Framework 1.1 版的用戶端可以使用 CAO 模式來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="19320-107">Instead, clients that have installed the .NET Framework version 1.1 can call it in CAO mode.</span></span> <span data-ttu-id="19320-108">如果協力廠商用戶端需要透過 WSDL 存取您的 XML web service，您必須允許匿名存取。</span><span class="sxs-lookup"><span data-stu-id="19320-108">If third-party clients need to access your XML web service via WSDL, you must allow anonymous access.</span></span>

 

> [!Note]  
> <span data-ttu-id="19320-109">若要使用 SSL 通訊協定來建立安全的通道，您必須取得並安裝 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="19320-109">To use the SSL protocol to establish a secure communication channel, you must obtain and install an SSL certificate.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="19320-110">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="19320-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="19320-111">若要選取 XML web service 的驗證機制，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="19320-111">To select the authentication mechanism for an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="19320-112">以滑鼠右鍵按一下桌面上的 **我的電腦** 圖示，然後按一下 [ **管理**]。</span><span class="sxs-lookup"><span data-stu-id="19320-112">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="19320-113">在 [ **服務和應用程式** ] 和 [ **網際網路資訊服務**] 下，找出對應至 XML web Service 之虛擬根目錄的圖示。</span><span class="sxs-lookup"><span data-stu-id="19320-113">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="19320-114">以滑鼠右鍵按一下目錄圖示，然後選擇 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="19320-114">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="19320-115">在 [內容] 對話方塊的 [ **目錄安全性** ] 索引標籤上，尋找 [ **驗證和存取控制** ]，然後按一下對應的 [ **編輯** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="19320-115">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span>

4.  <span data-ttu-id="19320-116">在 [ **驗證方法** ] 對話方塊中，于 [ **已驗證的存取**] 下，使用核取方塊來選取您想要允許的驗證機制。</span><span class="sxs-lookup"><span data-stu-id="19320-116">In the **Authentication Methods** dialog box, under **Authenticated access**, use the check boxes to select the authentication mechanisms you wish to allow.</span></span> <span data-ttu-id="19320-117">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="19320-117">Click **OK**.</span></span>

    > [!Note]  
    > <span data-ttu-id="19320-118">您可以使用 [IIS **驗證方法** ] 對話方塊上的下列任何選項，將 iis 設定為驗證呼叫者： **整合式 Windows 驗證**、 **Windows 網域伺服器的摘要式驗證**、 **基本驗證 (密碼是以純文字傳送)** 或 **.net Passport 驗證**。</span><span class="sxs-lookup"><span data-stu-id="19320-118">You can configure IIS to authenticate callers by using any of the following options on the IIS **Authentication Methods** dialog: **Integrated Windows authentication**, **Digest authentication for Windows domain servers**, **Basic authentication (password is sent in clear text)**, or **.NET Passport authentication**.</span></span> <span data-ttu-id="19320-119">您也可以允許匿名存取。</span><span class="sxs-lookup"><span data-stu-id="19320-119">You can also allow anonymous access.</span></span>

     

5.  <span data-ttu-id="19320-120">在 [屬性] 對話方塊中，按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="19320-120">In the properties dialog, click **OK**.</span></span>

<span data-ttu-id="19320-121">若要允許非安全、匿名存取 XML web service，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="19320-121">To allow nonsecure, anonymous access to an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="19320-122">以滑鼠右鍵按一下桌面上的 **我的電腦** 圖示，然後按一下 [ **管理**]。</span><span class="sxs-lookup"><span data-stu-id="19320-122">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="19320-123">在 [ **服務和應用程式** ] 和 [ **網際網路資訊服務**] 下，找出對應至 XML web Service 之虛擬根目錄的圖示。</span><span class="sxs-lookup"><span data-stu-id="19320-123">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="19320-124">以滑鼠右鍵按一下目錄圖示，然後選擇 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="19320-124">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="19320-125">在 [內容] 對話方塊的 [ **目錄安全性** ] 索引標籤上，尋找 [ **驗證和存取控制**]，然後按一下對應的 [ **編輯** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="19320-125">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="19320-126">選取 [ **啟用匿名存取** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="19320-126">Select the **Enable anonymous access** check box.</span></span> <span data-ttu-id="19320-127">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="19320-127">Click **OK**.</span></span>

4.  <span data-ttu-id="19320-128">在 [內容] 對話方塊的 [ **目錄安全性** ] 索引標籤上，找出 **安全通訊** ，然後按一下對應的 [ **編輯** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="19320-128">On the **Directory Security** tab of the properties dialog, locate **Secure communications** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="19320-129">取消核取 [ **需要安全通道 (SSL)** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="19320-129">Uncheck the **Require secure channel (SSL)** check box.</span></span> <span data-ttu-id="19320-130">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="19320-130">Click **OK**.</span></span>

5.  <span data-ttu-id="19320-131">在 [屬性] 對話方塊中，按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="19320-131">In the properties dialog, click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="19320-132">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="19320-132">Visual Basic</span></span>

<span data-ttu-id="19320-133">不適用。</span><span class="sxs-lookup"><span data-stu-id="19320-133">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="19320-134">C/C++</span><span class="sxs-lookup"><span data-stu-id="19320-134">C/C++</span></span>

<span data-ttu-id="19320-135">不適用。</span><span class="sxs-lookup"><span data-stu-id="19320-135">Does not apply.</span></span>

## <a name="additional-security-considerations"></a><span data-ttu-id="19320-136">其他安全性考慮</span><span class="sxs-lookup"><span data-stu-id="19320-136">Additional Security Considerations</span></span>

<span data-ttu-id="19320-137">藉由要求安全通道，您可以藉由加密用戶端和 XML web 服務之間的通訊，來協助保護交換的資料機密性。</span><span class="sxs-lookup"><span data-stu-id="19320-137">By requiring a secure channel, you help protect the confidentiality of the data exchanged by encrypting the communications between the client and your XML web service.</span></span> <span data-ttu-id="19320-138">如果您允許使用純文字密碼進行驗證，則應該要求安全通道以避免在網路上公開密碼。</span><span class="sxs-lookup"><span data-stu-id="19320-138">If you allow authentication using clear text passwords, you should require a secure channel in order to avoid exposing passwords on the network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19320-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="19320-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19320-140">以 CAO 模式存取 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="19320-140">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="19320-141">在 WKO 模式中存取 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="19320-141">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="19320-142">COM + SOAP 服務安全性考慮</span><span class="sxs-lookup"><span data-stu-id="19320-142">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="19320-143">建立 XML Web Service</span><span class="sxs-lookup"><span data-stu-id="19320-143">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> </dl>

 

 




---
title: 設定名稱服務
description: 從 Windows 2000 開始，當您安裝 Windows SDK 時，安裝程式會自動選取 Microsoft 定位器作為名稱服務提供者。 您可以透過主控台變更名稱服務提供者。
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462201"
---
# <a name="configuring-the-name-service"></a><span data-ttu-id="8f071-104">設定名稱服務</span><span class="sxs-lookup"><span data-stu-id="8f071-104">Configuring the Name Service</span></span>

<span data-ttu-id="8f071-105">從 Windows 2000 開始，當您安裝 Windows SDK 時，安裝程式會自動選取 Microsoft 定位器作為名稱服務提供者。</span><span class="sxs-lookup"><span data-stu-id="8f071-105">Starting with Windows 2000, when you install the Windows SDK, the setup program automatically selects Microsoft Locator as the name service provider.</span></span> <span data-ttu-id="8f071-106">您可以透過主控台變更名稱服務提供者。</span><span class="sxs-lookup"><span data-stu-id="8f071-106">You can change the name service provider through Control Panel.</span></span>

<span data-ttu-id="8f071-107">執行 nsid 的主機電腦會作為 DCE Cell Directory 服務的閘道，並在執行 Microsoft 作業系統和 DCE 電腦的電腦之間傳遞 NSI 函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="8f071-107">The host computer that runs the nsid acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="8f071-108">網路位址最多可有80個字元，例如，11.1.9.169 是有效的位址。</span><span class="sxs-lookup"><span data-stu-id="8f071-108">A network address can be up to 80 characters—for example, 11.1.9.169 is a valid address.</span></span>

> [!Note]  
> <span data-ttu-id="8f071-109">您必須擁有數位設備公司的 DCE CD 產品，才能將 DCE CD 設定為您的名稱服務提供者。</span><span class="sxs-lookup"><span data-stu-id="8f071-109">You must have the Digital Equipment Corporation DCE CDS product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="8f071-110">請參閱數位設備公司提供的檔，以取得 DCE CD 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8f071-110">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

 

<span data-ttu-id="8f071-111">**重新設定名稱服務提供者**</span><span class="sxs-lookup"><span data-stu-id="8f071-111">**To reconfigure the name service provider**</span></span>

1.  <span data-ttu-id="8f071-112">在主控台中，按一下 [ **網路** 連線] 圖示。</span><span class="sxs-lookup"><span data-stu-id="8f071-112">In Control Panel, click the **Network Connections** icon.</span></span> <span data-ttu-id="8f071-113">[ **網路** 連線] 視窗隨即出現。</span><span class="sxs-lookup"><span data-stu-id="8f071-113">The **Network Connections** window appears.</span></span>
2.  <span data-ttu-id="8f071-114">選取要設定的網路連線，按一下滑鼠右鍵， **然後從操作** 功能表中選取 [內容]。</span><span class="sxs-lookup"><span data-stu-id="8f071-114">Select the network connection to configure, right-click, and select **Properties** from the context menu.</span></span> <span data-ttu-id="8f071-115">[ **連接屬性** ] 對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="8f071-115">The **Connection Properties** dialog appears.</span></span>
3.  <span data-ttu-id="8f071-116">在 [ **連接屬性** ] 對話方塊中，選取 [ **Microsoft 網路用戶端** ]，然後按一下 [ **屬性** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="8f071-116">In the **Connection Properties** dialog, select **Client for Microsoft Networks** and click the **Properties** button.</span></span> <span data-ttu-id="8f071-117">[ **Microsoft 網路的用戶端屬性** ] 對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="8f071-117">The **Client for Microsoft Network Properties** dialog appears.</span></span>
4.  <span data-ttu-id="8f071-118">在 [ **Microsoft 網路的用戶端] 屬性** 對話方塊中，開啟 [ **名稱服務提供者** ] 下拉式清單，並從清單中選取名稱提供者。</span><span class="sxs-lookup"><span data-stu-id="8f071-118">In the **Client for Microsoft Network Properties** dialog, open the **Name service provider** drop-down and select a name provider from the list.</span></span>
    1.  <span data-ttu-id="8f071-119">當您選取 [Microsoft 定位器] 時，按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="8f071-119">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="8f071-120">完成設定程式。</span><span class="sxs-lookup"><span data-stu-id="8f071-120">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="8f071-121">當您選取 [DCE Cell Directory 服務，請在 [ **網路位址** ] 方塊中，輸入執行 NSI daemon (nsid) 的主電腦名稱稱，然後按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="8f071-121">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

<span data-ttu-id="8f071-122">**重新設定 Windows 2000 的名稱服務提供者**</span><span class="sxs-lookup"><span data-stu-id="8f071-122">**To reconfigure the name service provider for Windows 2000**</span></span>

1.  <span data-ttu-id="8f071-123">在主控台中，按一下 [ **網路** ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="8f071-123">In Control Panel, click the **Network** icon.</span></span>

    <span data-ttu-id="8f071-124">[ **網路** ] 對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="8f071-124">The **Network** dialog box appears.</span></span>

2.  <span data-ttu-id="8f071-125">在 [ **網路** ] 對話方塊中，按一下 [ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="8f071-125">In the **Network** dialog box, click **Configure**.</span></span>
3.  <span data-ttu-id="8f071-126">在 [ **NetworkSoftware** ] 清單中選取 [ **RPC** 設定]。</span><span class="sxs-lookup"><span data-stu-id="8f071-126">In the **NetworkSoftware** list, select **RPC Configuration**.</span></span>

    <span data-ttu-id="8f071-127">[ **RPC 名稱服務提供者** 設定] 對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="8f071-127">The **RPC Name Service Provider Configuration** dialog box appears.</span></span>

4.  <span data-ttu-id="8f071-128">在 [ **RPC 名稱服務提供者** 設定] 對話方塊中，從清單中選取名稱服務提供者。</span><span class="sxs-lookup"><span data-stu-id="8f071-128">In the **RPC Name Service Provider Configuration** dialog box, select a name service provider from the list.</span></span>
    1.  <span data-ttu-id="8f071-129">當您選取 [Microsoft 定位器] 時，按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="8f071-129">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="8f071-130">完成設定程式。</span><span class="sxs-lookup"><span data-stu-id="8f071-130">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="8f071-131">當您選取 [DCE Cell Directory 服務，請在 [ **網路位址** ] 方塊中，輸入執行 NSI daemon (nsid) 的主電腦名稱稱，然後按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="8f071-131">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

 

 





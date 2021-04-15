---
description: 指定驗證通訊協定
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: 指定驗證通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9bb2ec20df1ec398f32f3a1ee17334c10d9735
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468297"
---
# <a name="specifying-the-authentication-protocol"></a><span data-ttu-id="e3439-103">指定驗證通訊協定</span><span class="sxs-lookup"><span data-stu-id="e3439-103">Specifying the Authentication Protocol</span></span>

<span data-ttu-id="e3439-104">視您網站的安全性需求而定，您可以要求已排入佇列的元件服務一律驗證用戶端的身分識別、永遠不要驗證用戶端的身分識別，或只有在元件已設定為需要驗證時，才會驗證用戶端的身分識別，即使未透過佇列存取也是一樣。</span><span class="sxs-lookup"><span data-stu-id="e3439-104">Depending on the security requirements at your site, you can require the queued components service always to verify a client's identity, never to verify a client's identity, or to verify a client's identity only if the component is configured to require authentication even when not accessed through a queue.</span></span>

> [!Note]  
> <span data-ttu-id="e3439-105">若要在工作組模式中使用已排入佇列的元件，驗證等級必須設定為 [無]。</span><span class="sxs-lookup"><span data-stu-id="e3439-105">In order to use a queued component in workgroup mode, the authentication level must be set to none.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="e3439-106">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="e3439-106">Component Services Administrative Tool</span></span>

<span data-ttu-id="e3439-107">若要指定驗證通訊協定，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="e3439-107">To specify the authentication protocol, use the following steps:</span></span>

1.  <span data-ttu-id="e3439-108">在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="e3439-108">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="e3439-109">以滑鼠右鍵按一下您要指定驗證通訊協定的佇列應用程式，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="e3439-109">Right-click the queued application for which you want to specify the authentication protocol, and then click **Properties**.</span></span>

3.  <span data-ttu-id="e3439-110">在 [屬性] 對話方塊中，選取 [ **佇列** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="e3439-110">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="e3439-111">在 [ **MSMQ 訊息驗證**] 底下，選取與您要執行的驗證通訊協定相關聯的選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="e3439-111">Under **MSMQ Message Authentication**, select the radio button associated with the authentication protocol you want to implement.</span></span>

5.  <span data-ttu-id="e3439-112">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="e3439-112">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="e3439-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e3439-113">Visual Basic</span></span>

<span data-ttu-id="e3439-114">啟用已排入佇列的應用程式時，請使用 *AuthLevel* 參數，如 [使用佇列名字標記](using-the-queue-moniker.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e3439-114">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="cc"></a><span data-ttu-id="e3439-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="e3439-115">C/C++</span></span>

<span data-ttu-id="e3439-116">啟用已排入佇列的應用程式時，請使用 *AuthLevel* 參數，如 [使用佇列名字標記](using-the-queue-moniker.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e3439-116">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3439-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3439-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3439-118">已排入佇列的元件安全性</span><span class="sxs-lookup"><span data-stu-id="e3439-118">Queued Components Security</span></span>](queued-components-security.md)
</dt> <dt>

[<span data-ttu-id="e3439-119">工作組模式中的安全性限制</span><span class="sxs-lookup"><span data-stu-id="e3439-119">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 




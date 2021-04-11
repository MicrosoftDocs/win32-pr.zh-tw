---
title: 發行 COM + 服務
description: 以 COM 為基礎的服務會以 Windows installer (MSI) 封裝的形式提供應用程式 proxy。
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- 發行 COM + 服務
- Active Directory、使用、發行服務、COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020834"
---
# <a name="publishing-com-services"></a><span data-ttu-id="e0354-105">發行 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="e0354-105">Publishing COM+ Services</span></span>

<span data-ttu-id="e0354-106">以 COM 為基礎的服務會以 Windows installer (MSI) 封裝的形式提供應用程式 proxy。</span><span class="sxs-lookup"><span data-stu-id="e0354-106">COM-based services provide an application-proxy in the form of a Windows installer (MSI) package.</span></span> <span data-ttu-id="e0354-107">這個 .msi 檔案包含要使用的伺服器名稱，以及其他必要的元素，例如封送處理所需的 proxy/stub 和類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="e0354-107">This .msi file contains the server name to be used and other required elements, such as proxy/stubs and type libraries required for marshalling.</span></span> <span data-ttu-id="e0354-108">[元件服務] 嵌入式管理單元會自動產生 COM + 伺服器應用程式的這些應用程式 proxy。</span><span class="sxs-lookup"><span data-stu-id="e0354-108">The Component Services snap-in auto-generate these application proxies for COM+ Server applications.</span></span>

<span data-ttu-id="e0354-109">應用程式 proxy 會使用群組原則編輯器，發佈到 Active Directory 的原則物件中。</span><span class="sxs-lookup"><span data-stu-id="e0354-109">The application proxies are published into policy objects in Active Directory using the Group Policy Editor.</span></span> <span data-ttu-id="e0354-110">用戶端應用程式不需要任何特殊介入。</span><span class="sxs-lookup"><span data-stu-id="e0354-110">No special intervention is required in the client application.</span></span> <span data-ttu-id="e0354-111">用戶端電腦上的電腦/使用者帳戶必須位於設定為使用發行應用程式 proxy 之原則物件的 OU 中。</span><span class="sxs-lookup"><span data-stu-id="e0354-111">The computer/user account on the client computer must be in an OU configured to use the policy object in which the application proxies are published.</span></span> <span data-ttu-id="e0354-112">當用戶端建立相關物件的實例時，COM 系結器會自動透過目錄來尋找伺服器。</span><span class="sxs-lookup"><span data-stu-id="e0354-112">The COM binder automatically locates the server by means of the directory when the client establishes an instance of the objects concerned.</span></span>

 

 





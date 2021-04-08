---
title: 連接到 Active Directory
description: 有數種方法可用來存取 Active Directory。
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- 連接至 Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931851"
---
# <a name="connecting-to-active-directory"></a><span data-ttu-id="08fad-104">連接到 Active Directory</span><span class="sxs-lookup"><span data-stu-id="08fad-104">Connecting to Active Directory</span></span>

<span data-ttu-id="08fad-105">有數種方法可用來存取 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="08fad-105">There are several methods used to access Active Directory.</span></span> <span data-ttu-id="08fad-106">建議您使用 ADSI API 來存取 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="08fad-106">It is recommended that you use the ADSI API to access Active Directory.</span></span> <span data-ttu-id="08fad-107">ADSI 會執行 LDAP 通訊協定，以與 Active Directory 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="08fad-107">ADSI implements the LDAP protocol to communicate with Active Directory.</span></span> <span data-ttu-id="08fad-108">下列程式碼範例示範如何存取 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="08fad-108">The following code examples show how to access Active Directory.</span></span>


```VB
Set ns = GetObject("LDAP:")
```



<span data-ttu-id="08fad-109">這會開啟 LDAP 提供者，並將它準備好取出資料。</span><span class="sxs-lookup"><span data-stu-id="08fad-109">This opens the LDAP provider and prepares it to retrieve data.</span></span> <span data-ttu-id="08fad-110">在要求資料之前，不會建立連接。</span><span class="sxs-lookup"><span data-stu-id="08fad-110">No connection is established until data is requested.</span></span> <span data-ttu-id="08fad-111">當要求資料時，ADSI 在定位器服務的協助下，會嘗試找出最適合的網域控制站 (DC) 來進行連線，並建立與伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="08fad-111">When data is requested, ADSI, with the help of the locator service, attempts to find the best domain controller (DC) for the connection and will establish a connection to the server.</span></span> <span data-ttu-id="08fad-112">此進程稱為無伺服器系結。</span><span class="sxs-lookup"><span data-stu-id="08fad-112">This process is known as serverless binding.</span></span>

<span data-ttu-id="08fad-113">ADSI 也可讓您指定要用於連接的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="08fad-113">ADSI also enables you to specify the server name to use for the connection.</span></span>


```VB
Set obj = GetObject("LDAP://mysrv01")
```



<span data-ttu-id="08fad-114">在另一個案例中，您可能只知道功能變數名稱，但不知道特定的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="08fad-114">In another scenario, you may only know the domain name but not the specific server name.</span></span> <span data-ttu-id="08fad-115">同樣地，ADSI 還可讓您指定功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="08fad-115">Again, ADSI enables you to specify the domain name.</span></span> <span data-ttu-id="08fad-116">在 Windows 2000 中，功能變數名稱會以 DNS 名稱表示。</span><span class="sxs-lookup"><span data-stu-id="08fad-116">In Windows 2000, the domain name is represented as a DNS name.</span></span> <span data-ttu-id="08fad-117">例如，如果 Joe Worden （網路系統管理員）選擇使用功能變數名稱進行連線，他就可以使用下列程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="08fad-117">For example, if Joe Worden, the network administrator, chooses to connect using the domain name, he could use the following code example.</span></span>


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



<span data-ttu-id="08fad-118">ADSI 會連接到 fabrikam.com 網域中的其中一個網域控制站。</span><span class="sxs-lookup"><span data-stu-id="08fad-118">ADSI will connect to one of the domain controllers in the fabrikam.com domain.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08fad-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="08fad-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08fad-120">系結至 Active Directory 物件</span><span class="sxs-lookup"><span data-stu-id="08fad-120">Binding to Active Directory Objects</span></span>](binding-to-active-directory-objects.md)
</dt> </dl>

 

 





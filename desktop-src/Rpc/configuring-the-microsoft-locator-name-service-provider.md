---
title: 設定 Microsoft 定位器名稱服務提供者
description: 您可以藉由編輯 Rpcreg .dat 設定檔（其中包含 NSP 參數和 RPC 通訊協定設定）來變更您指定的名稱服務提供者。 使用文字編輯器來變更 NSP 專案。
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a5334436ce307030048a862f1375a91000b41e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301255"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a><span data-ttu-id="f22bc-104">設定 Microsoft 定位器名稱服務提供者</span><span class="sxs-lookup"><span data-stu-id="f22bc-104">Configuring the Microsoft Locator Name Service Provider</span></span>

<span data-ttu-id="f22bc-105">您可以藉由編輯 Rpcreg .dat 設定檔（其中包含 NSP 參數和 RPC 通訊協定設定）來變更您指定的名稱服務提供者。</span><span class="sxs-lookup"><span data-stu-id="f22bc-105">You can change the name service provider you specified by editing the Rpcreg.dat configuration file, which contains the NSP parameters and RPC protocol settings.</span></span> <span data-ttu-id="f22bc-106">使用文字編輯器來變更 NSP 專案。</span><span class="sxs-lookup"><span data-stu-id="f22bc-106">Use a text editor to change NSP entries.</span></span>

<span data-ttu-id="f22bc-107">**若要重新設定 Microsoft 定位器名稱服務提供者**</span><span class="sxs-lookup"><span data-stu-id="f22bc-107">**To reconfigure the Microsoft Locator name service provider**</span></span>

1.  <span data-ttu-id="f22bc-108">使用文字編輯器開啟 Rpcreg .dat 檔案。</span><span class="sxs-lookup"><span data-stu-id="f22bc-108">Open the Rpcreg.dat file using a text editor.</span></span>

    <span data-ttu-id="f22bc-109">除非您在安裝期間指定不同的路徑，否則 Rpcreg 會在根目錄中。</span><span class="sxs-lookup"><span data-stu-id="f22bc-109">Rpcreg.dat is in the root directory unless you specified a different path during setup.</span></span>

2.  <span data-ttu-id="f22bc-110">設定登錄專案的下列值。</span><span class="sxs-lookup"><span data-stu-id="f22bc-110">Set the following values for the registry entries.</span></span> 

    | <span data-ttu-id="f22bc-111">登錄項目</span><span class="sxs-lookup"><span data-stu-id="f22bc-111">Registry entry</span></span>                                         | <span data-ttu-id="f22bc-112">值</span><span class="sxs-lookup"><span data-stu-id="f22bc-112">Value</span></span>                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f22bc-113">軟體 \\ Microsoft \\ RPC \\ NameService \\ 通訊協定</span><span class="sxs-lookup"><span data-stu-id="f22bc-113">Software\\Microsoft\\RPC \\NameService\\Protocol</span></span>       | <span data-ttu-id="f22bc-114">您正在使用之通訊協定的通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="f22bc-114">The protocol sequence for the protocol you are using.</span></span> <span data-ttu-id="f22bc-115">預設值為 **ncacn \_ np**。</span><span class="sxs-lookup"><span data-stu-id="f22bc-115">The default is **ncacn\_np**.</span></span>                                                                   |
    | <span data-ttu-id="f22bc-116">Software \\ Microsoft \\ RPC \\ NameService \\ networkaddress.cache.ttl</span><span class="sxs-lookup"><span data-stu-id="f22bc-116">Software\\Microsoft\\RPC\\ NameService\\NetworkAddress</span></span> | <span data-ttu-id="f22bc-117">在名稱服務查閱作業期間，用戶端所使用之執行定位器的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="f22bc-117">The name of the computer running Locator that is used by clients during name service lookup operations.</span></span> <span data-ttu-id="f22bc-118">預設值是主域控制站。</span><span class="sxs-lookup"><span data-stu-id="f22bc-118">The default is the primary domain controller.</span></span> |
    | <span data-ttu-id="f22bc-119">軟體 \\ Microsoft \\ RPC \\ NameService \\ 端點</span><span class="sxs-lookup"><span data-stu-id="f22bc-119">Software\\Microsoft\\RPC\\ NameService\\Endpoint</span></span>       | <span data-ttu-id="f22bc-120">名稱服務所使用之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="f22bc-120">The name of the endpoint used by the name service.</span></span> <span data-ttu-id="f22bc-121">預設值為 [ \\ 管道 \\ 定位器]。</span><span class="sxs-lookup"><span data-stu-id="f22bc-121">The default is \\pipe\\locator.</span></span>                                                                    |

    

     

3.  <span data-ttu-id="f22bc-122">儲存並關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="f22bc-122">Save and close the file.</span></span>

 

 





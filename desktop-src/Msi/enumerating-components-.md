---
description: 在 Windows Server 2008 R2 或 Windows 7 上執行的 Windows Installer 5.0 可以列舉電腦上所安裝的所有元件，並取得元件的金鑰路徑。
ms.assetid: a6676340-1695-48c7-a1e4-7a02a7bc3fef
title: 列舉元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea314ee91c35fb021f5a8da64b6430e8cf950ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692387"
---
# <a name="enumerating-components"></a><span data-ttu-id="d63ff-103">列舉元件</span><span class="sxs-lookup"><span data-stu-id="d63ff-103">Enumerating Components</span></span>

<span data-ttu-id="d63ff-104">在 Windows Server 2008 R2 或 Windows 7 上執行的 Windows Installer 5.0 可以列舉電腦上所安裝的所有元件，並取得元件的金鑰路徑。</span><span class="sxs-lookup"><span data-stu-id="d63ff-104">Windows Installer 5.0 running on Windows Server 2008 R2 or Windows 7 can enumerate all components installed on the computer and obtain the key path for the component.</span></span> <span data-ttu-id="d63ff-105">針對 Windows Installer 5.0 撰寫的封裝可以使用 [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)、 [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)和 [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) 函式，在使用者帳戶和安裝內容之間搜尋元件和產品。</span><span class="sxs-lookup"><span data-stu-id="d63ff-105">A package authored for Windows Installer 5.0 can use the [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa), [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa), and [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) functions to search for components and products across user accounts and installation contexts.</span></span> <span data-ttu-id="d63ff-106">[**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)、 [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)和 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)函式只會傳回針對呼叫函式之使用者帳戶所安裝之元件和產品的資訊。</span><span class="sxs-lookup"><span data-stu-id="d63ff-106">The [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa), [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa), and [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) functions only return information for components and products installed for the user account that called the function.</span></span> <span data-ttu-id="d63ff-107">針對每個使用者帳戶，多次呼叫這些函式至少需要一次，才能收集整個電腦的資訊。</span><span class="sxs-lookup"><span data-stu-id="d63ff-107">Multiple calls to these functions, at least once for each user account, are required to collect information for the entire computer.</span></span>

<span data-ttu-id="d63ff-108">[**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)函式會列舉已安裝的元件。</span><span class="sxs-lookup"><span data-stu-id="d63ff-108">The [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa) function enumerates installed components.</span></span> <span data-ttu-id="d63ff-109">函式會在每次呼叫時，捕獲一個元件程式碼。</span><span class="sxs-lookup"><span data-stu-id="d63ff-109">The function retrieves one component code each time it is called.</span></span> <span data-ttu-id="d63ff-110">[**元件物件**](components.md)會透過此函式接收已安裝元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d63ff-110">The [**Component Object**](components.md) receives information about an installed component by this function.</span></span>

<span data-ttu-id="d63ff-111">[**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)函式會列舉屬於指定已安裝元件之用戶端的產品。</span><span class="sxs-lookup"><span data-stu-id="d63ff-111">The [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa) function enumerates products that are clients of a specified installed component.</span></span> <span data-ttu-id="d63ff-112">[**用戶端物件**](client.md)會透過此函數接收用戶端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d63ff-112">The [**Client Object**](client.md) receives information about a client by this function.</span></span>

<span data-ttu-id="d63ff-113">[**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)函式會傳回已安裝元件的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="d63ff-113">The [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) function returns the full path to an installed component.</span></span> <span data-ttu-id="d63ff-114">如果元件的金鑰路徑是登錄機碼，則函式會傳回登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d63ff-114">The function returns the registry key if the key path for the component is a registry key.</span></span> <span data-ttu-id="d63ff-115">[**ComponentInfo 物件**](componentinfo.md)會透過此函式接收已安裝元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d63ff-115">The [**ComponentInfo Object**](componentinfo.md) receives information about an installed component by this function.</span></span>

<span data-ttu-id="d63ff-116">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="d63ff-116">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="d63ff-117">從在 Windows 7 或 Windows Server 2008 R2 上執行的 Windows Installer 5.0 開始，可以使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="d63ff-117">This functionality is available beginning with Windows Installer 5.0 running on Windows 7 or Windows Server 2008 R2.</span></span>

 

 




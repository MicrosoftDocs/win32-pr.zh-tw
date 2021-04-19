---
description: 必須在系統上正確安裝傳輸通訊協定，並向 Windows 通訊端註冊，應用程式才能存取。
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: 同時存取多個傳輸通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989314"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a><span data-ttu-id="cbee5-103">同時存取多個傳輸通訊協定</span><span class="sxs-lookup"><span data-stu-id="cbee5-103">Simultaneous Access to Multiple Transport Protocols</span></span>

<span data-ttu-id="cbee5-104">必須在系統上正確安裝傳輸通訊協定，並向 Windows 通訊端註冊，應用程式才能存取。</span><span class="sxs-lookup"><span data-stu-id="cbee5-104">A transport protocol must be properly installed on the system and registered with Windows Sockets to be accessible to an application.</span></span> <span data-ttu-id="cbee5-105">Ws2 \_32.dll 程式庫會匯出一組函式來加速註冊程式。</span><span class="sxs-lookup"><span data-stu-id="cbee5-105">The Ws2\_32.dll library exports a set of functions to facilitate the registration process.</span></span> <span data-ttu-id="cbee5-106">這包括建立新的註冊，以及移除現有的註冊。</span><span class="sxs-lookup"><span data-stu-id="cbee5-106">This includes creating a new registration and removing an existing one.</span></span>

<span data-ttu-id="cbee5-107">建立新的註冊時，呼叫者 (亦即，堆疊廠商的安裝腳本) 會提供一或多個填入 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構，其中包含一組完整的通訊協定資訊。</span><span class="sxs-lookup"><span data-stu-id="cbee5-107">When new registrations are created, the caller (that is, the stack vendor's installation script) supplies one or more filled in [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures containing a complete set of information about the protocol.</span></span> <span data-ttu-id="cbee5-108">如需詳細資訊，請參閱 [Windows 通訊端 2 SPI](about-the-winsock-spi.md)。</span><span class="sxs-lookup"><span data-stu-id="cbee5-108">For more information, see [Windows Sockets 2 SPI](about-the-winsock-spi.md).</span></span> <span data-ttu-id="cbee5-109">以這種方式安裝的任何傳輸堆疊都稱為 Windows 通訊端服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cbee5-109">Any transport stack installed in this manner is referred to as a Windows Sockets service provider.</span></span>

<span data-ttu-id="cbee5-110">在 Windows XP Service Pack 2 (SP2) 、Windows Server 2003 （含 Service Pack 1） (SP1) ，以及 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="cbee5-110">On Windows XP with Service Pack 2 (SP2), Windows Server 2003 with Service Pack 1 (SP1), and Windows Vista and later.</span></span> <span data-ttu-id="cbee5-111">您可以使用下列命令，在命令提示字元中顯示包含已安裝的傳輸和命名空間提供者清單的 Winsock 目錄：</span><span class="sxs-lookup"><span data-stu-id="cbee5-111">the Winsock catalog that contains a list of installed transport and namespace providers can be displayed in a command prompt with the following command:</span></span>

<span data-ttu-id="cbee5-112">**netsh winsock show catalog**</span><span class="sxs-lookup"><span data-stu-id="cbee5-112">**netsh winsock show catalog**</span></span>

<span data-ttu-id="cbee5-113">Microsoft Windows 軟體開發套件 (SDK) 包含 *Sporder.exe*，可讓使用者查看和修改服務提供者的列舉順序。</span><span class="sxs-lookup"><span data-stu-id="cbee5-113">The Microsoft Windows Software Development Kit (SDK) includes *Sporder.exe*, which enables the user to view and modify the order in which service providers are enumerated.</span></span> <span data-ttu-id="cbee5-114">使用 *Sporder.exe*，如果有一個以上的這類堆疊存在，使用者就可以手動建立特定的 tcp/ip 通訊協定堆疊作為預設 tcp/ip 提供者。</span><span class="sxs-lookup"><span data-stu-id="cbee5-114">Using *Sporder.exe*, a user can manually establish a particular TCP/IP protocol stack as the default TCP/IP provider if more than one such stack is present.</span></span>

<span data-ttu-id="cbee5-115">*Sporder.exe* 應用程式會使用 *Sporder.dll* 中匯出的函式，來重新排序服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cbee5-115">The *Sporder.exe* application uses exported functions from *Sporder.dll* to reorder the service providers.</span></span> <span data-ttu-id="cbee5-116">因此，安裝應用程式可以使用 *Sporder.dll* 所提供的介面，以程式設計方式重新排序服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cbee5-116">As a result, installation applications can use the interface provided by *Sporder.dll* to programmatically reorder service providers.</span></span>

-   [<span data-ttu-id="cbee5-117">多層通訊協定和通訊協定鏈</span><span class="sxs-lookup"><span data-stu-id="cbee5-117">Layered Protocols and Protocol Chains</span></span>](layered-protocols-and-protocol-chains-2.md)
-   [<span data-ttu-id="cbee5-118">使用多個通訊協定</span><span class="sxs-lookup"><span data-stu-id="cbee5-118">Using Multiple Protocols</span></span>](using-multiple-protocols-2.md)
-   [<span data-ttu-id="cbee5-119">Select 上有多個提供者限制</span><span class="sxs-lookup"><span data-stu-id="cbee5-119">Multiple Provider Restrictions on Select</span></span>](multiple-provider-restrictions-on-select-2.md)

 

 

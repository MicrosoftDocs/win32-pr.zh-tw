---
title: 名稱服務應用程式指導方針
description: 當您開發分散式應用程式時，您需要為應用程式使用者提供方法，以指定在名稱服務資料庫中用來註冊應用程式的名稱。
ms.assetid: cda997b3-6031-4c0f-affc-c766ba4b7fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67af441da7a51917ae92751345e860e6b0fc92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932398"
---
# <a name="name-service-application-guidelines"></a><span data-ttu-id="9b3b0-103">名稱服務應用程式指導方針</span><span class="sxs-lookup"><span data-stu-id="9b3b0-103">Name Service Application Guidelines</span></span>

<span data-ttu-id="9b3b0-104">當您開發分散式應用程式時，您需要為應用程式使用者提供方法，以指定在名稱服務資料庫中用來註冊應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-104">When you develop your distributed application, you need to provide the application users with a method for specifying the name under which they can register the application in the name service database.</span></span> <span data-ttu-id="9b3b0-105">這個方法可以包含資料檔案、命令列輸入或對話方塊。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-105">This method can consist of a data file, command-line input, or dialog box.</span></span>

<span data-ttu-id="9b3b0-106">雖然 RPC 名稱服務架構支援各種方法來組織應用程式的伺服器專案，但它已針對查閱進行優化。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-106">Although the RPC name service architecture supports various methods for organizing an application's server entries, it is optimized for lookups.</span></span> <span data-ttu-id="9b3b0-107">因此，頻繁的更新可能會阻礙名稱服務和應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-107">As a result, frequent updates can hinder the performance of both the name service and the application.</span></span> <span data-ttu-id="9b3b0-108">若要避免不必要地匯出資訊，請選擇一個可讓伺服器判斷其資訊是否在名稱服務資料庫中的設計。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-108">To avoid exporting information unnecessarily, choose a design that lets the server determine whether its information is in the name service database.</span></span> <span data-ttu-id="9b3b0-109">此外，每個伺服器實例都應該匯出為它自己的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-109">In addition, each server instance should export to its own entry name.</span></span> <span data-ttu-id="9b3b0-110">否則，實例很難變更其支援的物件 Uuid 或通訊協定順序，而不會干擾另一個實例的資訊。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-110">Otherwise, it will be difficult for an instance to change its supported object UUIDs or protocol sequences without disturbing another instance's information.</span></span>

<span data-ttu-id="9b3b0-111">下列方法可避免這些錯誤，無論您的網路使用什麼名稱服務，都能提供良好的效能。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-111">The following method avoids these pitfalls and provides good performance, no matter what name service your network uses.</span></span>

<span data-ttu-id="9b3b0-112">首先，請設計您的應用程式，以便在第一次啟動給定的伺服器實例時，挑選唯一的伺服器專案名稱，並將此名稱連同應用程式的其他設定資訊儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-112">To begin with, design your application so that the first time a given server instance starts, it picks a unique server-entry name and saves this name in the registry along with the application's other configuration information.</span></span> <span data-ttu-id="9b3b0-113">然後，將其系結控制碼和物件 Uuid （如果有的話）匯出至其名稱服務專案。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-113">Then, have it export its binding handles and object UUIDs, if any, to its name service entry.</span></span>

<span data-ttu-id="9b3b0-114">後續的伺服器實例調用應該檢查名稱服務專案是否存在，並且包含一組正確的物件 Uuid 和系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-114">Subsequent invocations of the server instance should check that the name service entry is present and contains the correct set of object UUIDs and binding handles.</span></span> <span data-ttu-id="9b3b0-115">遺漏的專案可能表示系統管理員已將它移除，或電源中斷導致名稱服務資訊遺失。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-115">A missing entry may mean that an administrator removed it, or that a power outage caused the name service information to be lost.</span></span> <span data-ttu-id="9b3b0-116">請務必確認專案中的系結控制碼正確;例如，如果系統管理員將 TCP/IP 支援新增至電腦，則在呼叫 [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)時，RPC 伺服器將會接聽該通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-116">It is important to verify that the binding handles in the entry are correct; if an administrator adds TCP/IP support to a computer, for example, RPC servers will listen on that protocol sequence when they call [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs).</span></span> <span data-ttu-id="9b3b0-117">但是，如果伺服器未更新名稱服務專案，將不會通知用戶端支援 TCP。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-117">However, if the server does not update the name service entry, clients will not be informed that TCP is supported.</span></span>

<span data-ttu-id="9b3b0-118">當用戶端匯入時，它應該將 **Null** 指定為專案名稱。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-118">When the client imports, it should specify **NULL** as the entry name.</span></span> <span data-ttu-id="9b3b0-119">指定 **Null** 會導致 Microsoft RPC 程式庫函式在用戶端電腦的網域或工作組中的所有名稱服務專案中搜尋介面，進而尋找每個實例的資訊。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-119">Specifying **NULL** causes the Microsoft RPC library functions to search for the interface in all name service entries in the client computer's domain or workgroup, thus finding the information for every instance.</span></span>

<span data-ttu-id="9b3b0-120">如果您使用物件 Uuid 來代表已知的物件，例如印表機，則可以使用此方法的變化。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-120">If you use object UUIDs to represent well-known objects such as printers, you can use a variation of this method.</span></span> <span data-ttu-id="9b3b0-121">您可以設計應用程式，讓每個實例為每個支援的物件（例如 "/.：/）建立一個專案，而不是將系結匯出至一個專案。printers/Laser1 "和"/.：/印表機/Laser2」。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-121">Instead of exporting bindings to one entry, design your application so that each instance creates an entry for each supported object, such as "/.:/printers/Laser1" and "/.:/printers/Laser2."</span></span> <span data-ttu-id="9b3b0-122">然後，讓伺服器將其系結控制碼匯出至每個伺服器專案，以及與該專案相關的物件 UUID。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-122">Then, have the server export its binding handles to each server entry, along with the object UUID relevant to that entry.</span></span>

<span data-ttu-id="9b3b0-123">在此情況下，用戶端可以從相關的伺服器專案匯入，依名稱查閱資源;它不需要資源的物件 UUID。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-123">In this case, a client can look up a resource by name by importing from the relevant server entry; it does not require the object UUID of the resource.</span></span> <span data-ttu-id="9b3b0-124">如果它有資源 UUID 但沒有名稱，則可以從 **null** 專案匯入。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-124">If it has the resource UUID but not the name, it can import from the **null** entry.</span></span>

 

 





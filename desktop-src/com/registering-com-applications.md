---
title: 註冊 COM 應用程式
description: 註冊 COM 應用程式
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301783"
---
# <a name="registering-com-applications"></a><span data-ttu-id="a7ae2-103">註冊 COM 應用程式</span><span class="sxs-lookup"><span data-stu-id="a7ae2-103">Registering COM Applications</span></span>

<span data-ttu-id="a7ae2-104">登錄是系統資料庫，其中包含有關系統硬體和軟體的設定以及系統使用者的資訊。</span><span class="sxs-lookup"><span data-stu-id="a7ae2-104">The registry is a system database that contains information about the configuration of system hardware and software as well as about users of the system.</span></span> <span data-ttu-id="a7ae2-105">任何以 Windows 為基礎的程式都可以將資訊新增至登錄，然後從登錄中讀取資訊。</span><span class="sxs-lookup"><span data-stu-id="a7ae2-105">Any Windows-based program can add information to the registry and read information back from the registry.</span></span> <span data-ttu-id="a7ae2-106">用戶端會搜尋登錄以取得要使用的有趣元件。</span><span class="sxs-lookup"><span data-stu-id="a7ae2-106">Clients search the registry for interesting components to use.</span></span>

<span data-ttu-id="a7ae2-107">登錄會維護系統中安裝之所有 COM 物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a7ae2-107">The registry maintains information about all the COM objects installed in the system.</span></span> <span data-ttu-id="a7ae2-108">每當應用程式建立 COM 元件的實例時，系統會諮詢登錄以將元件的 CLSID 或 ProgID 解析成包含該元件的伺服器 DLL 或 EXE 的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="a7ae2-108">Whenever an application creates an instance of a COM component, the registry is consulted to resolve either the CLSID or ProgID of the component into the pathname of the server DLL or EXE that contains it.</span></span> <span data-ttu-id="a7ae2-109">在判斷元件的伺服器之後，Windows 會將伺服器載入用戶端應用程式的進程空間 (同進程元件) 或在其本身的進程空間 (本機和遠端伺服器) 啟動伺服器。</span><span class="sxs-lookup"><span data-stu-id="a7ae2-109">After determining the component's server, Windows either loads the server into the process space of the client application (in-process components) or starts the server in its own process space (local and remote servers).</span></span> <span data-ttu-id="a7ae2-110">伺服器會建立元件的實例，並將其中一個元件介面的參考傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="a7ae2-110">The server creates an instance of the component and returns to the client a reference to one of the component's interfaces.</span></span>

<span data-ttu-id="a7ae2-111">如需 Windows 登錄的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="a7ae2-111">For more information about the Windows registry, see the following topics:</span></span>

-   [<span data-ttu-id="a7ae2-112">登錄階層</span><span class="sxs-lookup"><span data-stu-id="a7ae2-112">Registry Hierarchy</span></span>](registry-hierarchy.md)
-   [<span data-ttu-id="a7ae2-113">類別和伺服器</span><span class="sxs-lookup"><span data-stu-id="a7ae2-113">Classes and Servers</span></span>](classes-and-servers.md)
-   [<span data-ttu-id="a7ae2-114">分類元件</span><span class="sxs-lookup"><span data-stu-id="a7ae2-114">Classifying Components</span></span>](classifying-components.md)
-   [<span data-ttu-id="a7ae2-115">使用 OleView</span><span class="sxs-lookup"><span data-stu-id="a7ae2-115">Using OleView</span></span>](using-oleview.md)
-   [<span data-ttu-id="a7ae2-116">註冊元件</span><span class="sxs-lookup"><span data-stu-id="a7ae2-116">Registering Components</span></span>](registering-components.md)
-   [<span data-ttu-id="a7ae2-117">正在檢查註冊</span><span class="sxs-lookup"><span data-stu-id="a7ae2-117">Checking Registration</span></span>](checking-registration.md)
-   [<span data-ttu-id="a7ae2-118">未知的使用者類型</span><span class="sxs-lookup"><span data-stu-id="a7ae2-118">Unknown User Types</span></span>](unknown-user-types.md)
-   [<span data-ttu-id="a7ae2-119">COM 登錄機碼</span><span class="sxs-lookup"><span data-stu-id="a7ae2-119">COM Registry Keys</span></span>](com-registry-keys.md)

 

 





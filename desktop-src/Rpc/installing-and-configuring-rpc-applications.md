---
title: 安裝和設定 RPC 應用程式
description: 當伺服器或用戶端上安裝 Microsoft Windows 作業系統時，安裝程式會自動安裝 RPC 執行時間檔案。
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- 遠端程序呼叫 RPC、工作、安裝和設定應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90837261c571276a74bb3a5354c7b9a5db2da6cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462465"
---
# <a name="installing-and-configuring-rpc-applications"></a><span data-ttu-id="620c9-104">安裝和設定 RPC 應用程式</span><span class="sxs-lookup"><span data-stu-id="620c9-104">Installing and Configuring RPC Applications</span></span>

<span data-ttu-id="620c9-105">當伺服器或用戶端上安裝 Microsoft Windows 作業系統時，安裝程式會自動安裝 RPC 執行時間檔案。</span><span class="sxs-lookup"><span data-stu-id="620c9-105">When the Microsoft Windows operating system is installed on a server or client, setup automatically installs the RPC run-time files.</span></span> <span data-ttu-id="620c9-106">不需要進一步的 RPC 安裝。</span><span class="sxs-lookup"><span data-stu-id="620c9-106">No further RPC installation is required.</span></span> <span data-ttu-id="620c9-107">不過，您必須確定您安裝的 Windows 版本支援分散式應用程式中使用的所有功能。</span><span class="sxs-lookup"><span data-stu-id="620c9-107">You must ensure, however, that the version of Windows you install supports all the features used in your distributed application.</span></span>

<span data-ttu-id="620c9-108">當您在 Windows 3.x 或 Microsoft MS-DOS 作業系統上使用 RPC 應用程式時，您必須將 RPC 執行時間可執行檔案複製到將使用應用程式的 Windows 3.x 或 MS-DOS 電腦上。</span><span class="sxs-lookup"><span data-stu-id="620c9-108">When you use an RPC application on a Windows 3.x or Microsoft MS-DOS operating system, you must copy the RPC run-time executable files to the Windows 3.x or MS-DOS computers that will be using the application.</span></span> <span data-ttu-id="620c9-109">\\ \\ \_ 平臺軟體發展工具組上的 directory mstools RPC rt16 (SDK) CD 包含這些檔案的磁片映射，以及安裝程式來安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="620c9-109">The directory \\mstools\\rpc\_rt16 on the Platform Software Development Kit (SDK) CD contains a disk image of these files along with a setup program to install the files.</span></span> <span data-ttu-id="620c9-110">使用這個磁片映射來建立安裝磁片，以便與您的 RPC 應用程式一起散發。</span><span class="sxs-lookup"><span data-stu-id="620c9-110">Use this disk image to create an install disk for distribution with your RPC application.</span></span> <span data-ttu-id="620c9-111">您也可以在32位/64 位的 Windows 作業系統上，使用以 MS-DOS 或 Windows 為目標的16位用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="620c9-111">You can also use 16-bit client applications targeted toward MS-DOS or Windows on a 32-bit/64-bit Windows operating system.</span></span> <span data-ttu-id="620c9-112">不過，您的應用程式安裝程式必須安裝此磁片映射中包含的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="620c9-112">However, your application's installation program must install the executable files contained in this disk image.</span></span>

<span data-ttu-id="620c9-113">當您為 Macintosh 用戶端建立 RPC 應用程式時，您必須在組建階段將必要的檔案連結到應用程式。</span><span class="sxs-lookup"><span data-stu-id="620c9-113">When you build an RPC application for a Macintosh client, you must link the necessary files to the application at build time.</span></span> <span data-ttu-id="620c9-114">不需要額外的 RPC 安裝。</span><span class="sxs-lookup"><span data-stu-id="620c9-114">No additional RPC installation is needed.</span></span>

<span data-ttu-id="620c9-115">如需可轉散發檔案和授權合約的詳細資訊，請參閱 \\ \\ \\ \\ Platform SDK CD 上的授權Redist.txt 和授權License.txt。</span><span class="sxs-lookup"><span data-stu-id="620c9-115">For more details about redistributable files and licensing agreements, see \\LICENSE\\Redist.txt and \\LICENSE\\License.txt on the Platform SDK CD.</span></span>

<span data-ttu-id="620c9-116">本節包含在各種不同的硬體和軟體平臺上設定 RPC 應用程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="620c9-116">This section contains information about setting up RPC applications on a variety of hardware and software platforms.</span></span> <span data-ttu-id="620c9-117">它會在下列各節中提供討論：</span><span class="sxs-lookup"><span data-stu-id="620c9-117">It presents the discussion in the following sections:</span></span>

-   [<span data-ttu-id="620c9-118">設定名稱服務提供者</span><span class="sxs-lookup"><span data-stu-id="620c9-118">Configuring the Name Service Provider</span></span>](configuring-the-name-service-provider.md)
-   [<span data-ttu-id="620c9-119">登錄資訊</span><span class="sxs-lookup"><span data-stu-id="620c9-119">Registry Information</span></span>](registry-information.md)
-   [<span data-ttu-id="620c9-120">使用 RPC 搭配 Winsock Proxy</span><span class="sxs-lookup"><span data-stu-id="620c9-120">Using RPC with Winsock Proxy</span></span>](using-rpc-with-winsock-proxy.md)
-   [<span data-ttu-id="620c9-121">SPX/IPX 安裝</span><span class="sxs-lookup"><span data-stu-id="620c9-121">SPX/IPX Installation</span></span>](spx-ipx-installation.md)
-   [<span data-ttu-id="620c9-122">設定安全性伺服器</span><span class="sxs-lookup"><span data-stu-id="620c9-122">Configuring the Security Server</span></span>](configuring-the-security-server.md)

 

 





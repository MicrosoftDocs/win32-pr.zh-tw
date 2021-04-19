---
title: 關於遠端存取服務管理
description: Windows 2000 和更新版本的作業系統提供一組功能，可在 RAS 伺服器上管理使用者權限和埠。
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- 路由及遠端存取服務 RRAS、RAS 管理
- 路由及遠端存取服務 RRAS、RAS 管理、描述
- RAS 系統管理 RRAS
- RAS 管理 RRAS，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106980265"
---
# <a name="about-remote-access-service-administration"></a><span data-ttu-id="07f37-107">關於遠端存取服務管理</span><span class="sxs-lookup"><span data-stu-id="07f37-107">About Remote Access Service Administration</span></span>

<span data-ttu-id="07f37-108">Windows 2000 和更新版本的作業系統提供一組功能，可在 RAS 伺服器上管理使用者權限和埠。</span><span class="sxs-lookup"><span data-stu-id="07f37-108">Windows 2000 and later operating systems provide a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="07f37-109">您可以使用這些功能來開發 RAS 伺服器管理應用程式，以執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="07f37-109">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="07f37-110">列舉擁有一組指定 RAS 許可權的使用者</span><span class="sxs-lookup"><span data-stu-id="07f37-110">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="07f37-111">指派或撤銷指定使用者的 RAS 許可權</span><span class="sxs-lookup"><span data-stu-id="07f37-111">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="07f37-112">列舉 RAS 伺服器上設定的埠</span><span class="sxs-lookup"><span data-stu-id="07f37-112">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="07f37-113">取得 RAS 伺服器上指定埠的相關資訊和統計資料</span><span class="sxs-lookup"><span data-stu-id="07f37-113">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="07f37-114">重設指定埠的統計資料計數器</span><span class="sxs-lookup"><span data-stu-id="07f37-114">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="07f37-115">中斷指定埠的連接</span><span class="sxs-lookup"><span data-stu-id="07f37-115">Disconnect a specified port</span></span>

<span data-ttu-id="07f37-116">您也可以安裝 RAS 伺服器管理 DLL 來審核使用者連線，並將 IP 位址指派給撥入使用者。</span><span class="sxs-lookup"><span data-stu-id="07f37-116">You can also install a RAS server administration DLL to audit user connections and assign IP addresses to dial-in users.</span></span> <span data-ttu-id="07f37-117">當使用者嘗試連線或中斷連線時，DLL 會匯出一組 RAS 伺服器所呼叫的函數。</span><span class="sxs-lookup"><span data-stu-id="07f37-117">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

<span data-ttu-id="07f37-118">本檔將說明下列主題：</span><span class="sxs-lookup"><span data-stu-id="07f37-118">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="07f37-119">函數比較： Windows 2000 與 RRAS 可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="07f37-119">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [<span data-ttu-id="07f37-120">RAS 使用者管理</span><span class="sxs-lookup"><span data-stu-id="07f37-120">RAS User Administration</span></span>](ras-user-administration.md)
-   [<span data-ttu-id="07f37-121">RAS 伺服器和埠管理</span><span class="sxs-lookup"><span data-stu-id="07f37-121">RAS Server and Port Administration</span></span>](ras-server-and-port-administration.md)
-   [<span data-ttu-id="07f37-122">RAS 系統管理 DLL</span><span class="sxs-lookup"><span data-stu-id="07f37-122">RAS Administration DLL</span></span>](ras-administration-dll.md)
-   [<span data-ttu-id="07f37-123">RAS 管理 DLL 登錄設定</span><span class="sxs-lookup"><span data-stu-id="07f37-123">RAS Administration DLL Registry Setup</span></span>](ras-administration-dll-registry-setup.md)

 

 





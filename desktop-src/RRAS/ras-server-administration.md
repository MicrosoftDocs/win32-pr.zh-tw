---
title: RAS 伺服器管理
description: Windows NT Server 4.0 提供一組功能，可在 Windows NT/Windows 2000 RAS 伺服器上管理使用者權限和埠。
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- 伺服器管理，RAS
- 管理，RAS 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183955"
---
# <a name="ras-server-administration"></a><span data-ttu-id="909d4-105">RAS 伺服器管理</span><span class="sxs-lookup"><span data-stu-id="909d4-105">RAS Server Administration</span></span>

<span data-ttu-id="909d4-106">Windows NT Server 4.0 提供一組功能，可在 Windows NT/Windows 2000 RAS 伺服器上管理使用者權限和埠。</span><span class="sxs-lookup"><span data-stu-id="909d4-106">Windows NT Server 4.0 provides a set of functions for administering user permissions and ports on Windows NT/Windows 2000 RAS servers.</span></span> <span data-ttu-id="909d4-107">Windows 95 不支援這些功能。</span><span class="sxs-lookup"><span data-stu-id="909d4-107">Windows 95 does not support these functions.</span></span> <span data-ttu-id="909d4-108">您可以使用這些功能來開發 RAS 伺服器管理應用程式，以執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="909d4-108">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="909d4-109">列舉擁有一組指定 RAS 許可權的使用者</span><span class="sxs-lookup"><span data-stu-id="909d4-109">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="909d4-110">指派或撤銷指定使用者的 RAS 許可權</span><span class="sxs-lookup"><span data-stu-id="909d4-110">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="909d4-111">列舉 RAS 伺服器上設定的埠</span><span class="sxs-lookup"><span data-stu-id="909d4-111">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="909d4-112">取得 RAS 伺服器上指定埠的相關資訊和統計資料</span><span class="sxs-lookup"><span data-stu-id="909d4-112">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="909d4-113">重設指定埠的統計資料計數器</span><span class="sxs-lookup"><span data-stu-id="909d4-113">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="909d4-114">中斷指定埠的連接</span><span class="sxs-lookup"><span data-stu-id="909d4-114">Disconnect a specified port</span></span>

<span data-ttu-id="909d4-115">您也可以安裝 RAS 伺服器管理 DLL 來審核使用者連線，以及將 IP 位址指派給撥入使用者。</span><span class="sxs-lookup"><span data-stu-id="909d4-115">You can also install a RAS server administration DLL for auditing user connections and assigning IP addresses to dial-in users.</span></span> <span data-ttu-id="909d4-116">當使用者嘗試連線或中斷連線時，DLL 會匯出一組 RAS 伺服器所呼叫的函數。</span><span class="sxs-lookup"><span data-stu-id="909d4-116">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

 

 





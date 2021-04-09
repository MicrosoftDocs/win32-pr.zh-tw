---
title: 自動撥號對應資料庫
description: 自動撥號對應資料庫會將網路位址對應到 RAS 電話簿專案。
ms.assetid: 4589d1e5-eec3-46ac-a10f-f20ae9f7b543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511f15f98848559a892e8c20e766d47a07780fbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842372"
---
# <a name="autodial-mapping-database"></a><span data-ttu-id="e6c98-103">自動撥號對應資料庫</span><span class="sxs-lookup"><span data-stu-id="e6c98-103">AutoDial Mapping Database</span></span>

<span data-ttu-id="e6c98-104">自動撥號對應資料庫會將網路位址對應到 RAS 電話簿專案。</span><span class="sxs-lookup"><span data-stu-id="e6c98-104">The AutoDial mapping database maps network addresses to RAS phone-book entries.</span></span> <span data-ttu-id="e6c98-105">資料庫可以包含 IP 位址 (例如 "172.21.167.35" ) 、網際網路主機名稱 (例如 "www.microsoft.com" ) 或 NetBIOS 名稱 (例如 "products1" ) 。</span><span class="sxs-lookup"><span data-stu-id="e6c98-105">The database can include IP addresses (for example, "172.21.167.35"), Internet host names (for example, "www.microsoft.com"), or NetBIOS names (for example, "products1").</span></span> <span data-ttu-id="e6c98-106">與自動撥號資料庫中每個位址相關聯的是一組一或多個 [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) 專案。</span><span class="sxs-lookup"><span data-stu-id="e6c98-106">Associated with each address in the AutoDial database is a set of one or more [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) entries.</span></span> <span data-ttu-id="e6c98-107">其中每個專案都會指定一個電話簿專案，讓 RAS 可以撥號來從特定的電話語音應用程式開發介面連接到位址， (TAPI) 撥號位置。</span><span class="sxs-lookup"><span data-stu-id="e6c98-107">Each of these entries specifies a phone-book entry that RAS can dial to connect to the address from a particular Telephony Application Programming Interface (TAPI) dialing location.</span></span> <span data-ttu-id="e6c98-108">如需有關 TAPI 撥號位置的詳細資訊，請參閱 TAPI 檔。</span><span class="sxs-lookup"><span data-stu-id="e6c98-108">For more information about TAPI dialing locations, see the TAPI documentation.</span></span>

<span data-ttu-id="e6c98-109">自動撥號會在兩種情況下自動在自動撥號對應資料庫中建立專案：</span><span class="sxs-lookup"><span data-stu-id="e6c98-109">AutoDial automatically creates entries in the AutoDial mapping database in two situations:</span></span>

-   <span data-ttu-id="e6c98-110">嘗試連接到網路位址失敗時</span><span class="sxs-lookup"><span data-stu-id="e6c98-110">When an attempt to connect to a network address fails</span></span>

    <span data-ttu-id="e6c98-111">如果對應資料庫的位址沒有任何專案，且電腦未直接或透過 RAS 連線到網路，自動撥號會提示使用者指定建立撥號連線所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="e6c98-111">If there is no entry for the address in the mapping database, and the computer is not connected to a network, either directly or through RAS, AutoDial prompts the user to specify the information necessary to establish a dial-up connection.</span></span> <span data-ttu-id="e6c98-112">如果使用者提供資訊，而且撥號連線作業成功，自動撥號會將資訊儲存在對應資料庫中。</span><span class="sxs-lookup"><span data-stu-id="e6c98-112">If the user provides the information and the dial-up connection operation is successful, AutoDial stores the information in the mapping database.</span></span>

-   <span data-ttu-id="e6c98-113">當電腦透過 RAS 連線到網路時</span><span class="sxs-lookup"><span data-stu-id="e6c98-113">When the computer is connected to a network through RAS</span></span>

    <span data-ttu-id="e6c98-114">當使用者連線到網路位址時，自動撥號會在資料庫中建立一個專案。</span><span class="sxs-lookup"><span data-stu-id="e6c98-114">Whenever the user connects to a network address, AutoDial creates an entry in the database.</span></span> <span data-ttu-id="e6c98-115">此專案會將網路位址對應到用來建立 RAS 連線的電話通訊錄專案。</span><span class="sxs-lookup"><span data-stu-id="e6c98-115">The entry maps the network address to the phone-book entry that was used to establish the RAS connection.</span></span>

<span data-ttu-id="e6c98-116">您可以使用 [**RasSetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) 函數將位址新增至自動撥號對應資料庫、從資料庫中刪除位址，或變更與資料庫中現有位址相關聯的自動撥號專案。</span><span class="sxs-lookup"><span data-stu-id="e6c98-116">You can use the [**RasSetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) function to add an address to the AutoDial mapping database, delete an address from the database, or change the AutoDial entries associated with an existing address in the database.</span></span> <span data-ttu-id="e6c98-117">您可以使用 [**RasGetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) 函式，在自動撥號對應資料庫中取出與指定的網路位址相關聯的自動撥號專案。</span><span class="sxs-lookup"><span data-stu-id="e6c98-117">You can use the [**RasGetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) function to retrieve the AutoDial entries associated with a specified network address in the AutoDial mapping database.</span></span> <span data-ttu-id="e6c98-118">[**RasEnumAutodialAddresses**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa)函數會傳回自動撥號對應資料庫中的所有地址清單。</span><span class="sxs-lookup"><span data-stu-id="e6c98-118">The [**RasEnumAutodialAddresses**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa) function returns a list of all addresses in the AutoDial mapping database.</span></span>

 

 
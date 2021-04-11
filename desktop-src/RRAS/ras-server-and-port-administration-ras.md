---
title: RAS 伺服器和埠管理
description: RAS 伺服器管理功能可讓您取得指定的 RAS 伺服器與其埠的相關資訊。 這些功能也可讓您在指定的 RAS 伺服器埠上終止連接。
ms.assetid: 783b0ded-7c0e-49eb-8040-563d5dd675f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af21dfeda38a1c1147bf864a1fa1959092ac946
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021721"
---
# <a name="ras-server-and-port-administration"></a><span data-ttu-id="1321b-104">RAS 伺服器和埠管理</span><span class="sxs-lookup"><span data-stu-id="1321b-104">RAS Server and Port Administration</span></span>

<span data-ttu-id="1321b-105">RAS 伺服器管理功能可讓您取得指定的 RAS 伺服器與其埠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1321b-105">The RAS server administration functions enable you to get information about a specified RAS server and its ports.</span></span> <span data-ttu-id="1321b-106">這些功能也可讓您在指定的 RAS 伺服器埠上終止連接。</span><span class="sxs-lookup"><span data-stu-id="1321b-106">These functions also enable you to terminate a connection on a specified RAS server port.</span></span>

<span data-ttu-id="1321b-107">[**RasAdminServerGetInfo**](rasadminservergetinfo.md)函式會傳回 [**ras \_ 伺服器 \_ 0**](ras-server-0-str.md)結構，其中包含 ras 伺服器設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1321b-107">The [**RasAdminServerGetInfo**](rasadminservergetinfo.md) function returns a [**RAS\_SERVER\_0**](ras-server-0-str.md) structure that contains information about the configuration of a RAS server.</span></span> <span data-ttu-id="1321b-108">傳回的資訊包括目前可用的埠數目、目前使用中的埠數目，以及伺服器版本號碼。</span><span class="sxs-lookup"><span data-stu-id="1321b-108">The returned information includes the number of ports currently available for connection, the number of ports currently in use, and the server version number.</span></span>

<span data-ttu-id="1321b-109">[**RasAdminPortEnum**](rasadminportenum.md)函式會抓取 [**ras \_ 埠 \_ 0**](ras-port-0-str.md)結構的陣列，其中包含 ras 伺服器上所設定之每個埠的資訊。</span><span class="sxs-lookup"><span data-stu-id="1321b-109">The [**RasAdminPortEnum**](rasadminportenum.md) function retrieves an array of [**RAS\_PORT\_0**](ras-port-0-str.md) structures that contains information for each of the ports configured on a RAS server.</span></span> <span data-ttu-id="1321b-110">每個埠的資訊包括：</span><span class="sxs-lookup"><span data-stu-id="1321b-110">The information for each port includes:</span></span>

-   <span data-ttu-id="1321b-111">埠的名稱</span><span class="sxs-lookup"><span data-stu-id="1321b-111">The name of the port</span></span>
-   <span data-ttu-id="1321b-112">連接到埠之裝置的相關資訊</span><span class="sxs-lookup"><span data-stu-id="1321b-112">Information about the device attached to the port</span></span>
-   <span data-ttu-id="1321b-113">與埠相關聯的 RAS 伺服器是否為 Windows NT/Windows 2000 伺服器</span><span class="sxs-lookup"><span data-stu-id="1321b-113">Whether the RAS server associated with the port is a Windows NT/Windows 2000 Server</span></span>
-   <span data-ttu-id="1321b-114">埠是否正在使用中，如果是，則連接的相關資訊</span><span class="sxs-lookup"><span data-stu-id="1321b-114">Whether the port is currently in use, and if it is, information about the connection</span></span>

<span data-ttu-id="1321b-115">您可以呼叫 [**RasAdminPortGetInfo**](rasadminportgetinfo.md) 函數，以取得有關 RAS 伺服器上指定埠的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="1321b-115">You can call the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function to get additional information about a specified port on a RAS server.</span></span> <span data-ttu-id="1321b-116">此函式會傳回包含 [**ras \_ 埠 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0)結構的 [**ras \_ 埠 \_ 1**](ras-port-1-str.md)結構，以及埠目前狀態的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1321b-116">This function returns a [**RAS\_PORT\_1**](ras-port-1-str.md) structure that contains a [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) structure and additional information about the current state of the port.</span></span> <span data-ttu-id="1321b-117">**RasAdminPortGetInfo** 函式也會傳回 [**RAS \_ 參數**](ras-parameters-str.md)結構的陣列，以描述與埠相關聯之任何媒體特定金鑰的值。</span><span class="sxs-lookup"><span data-stu-id="1321b-117">The **RasAdminPortGetInfo** function also returns an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures that describe the values of any media-specific keys associated with the port.</span></span> <span data-ttu-id="1321b-118">**Ras \_ 參數** 結構會使用 [**ras \_ PARAMS \_ 格式**](ras-params-format-str.md)列舉的值，來指出每個媒體特定索引鍵的值格式。</span><span class="sxs-lookup"><span data-stu-id="1321b-118">A **RAS\_PARAMETERS** structure uses a value from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration to indicate the format of the value for each media-specific key.</span></span>

<span data-ttu-id="1321b-119">[**RasAdminPortGetInfo**](rasadminportgetinfo.md)函式也會傳回 [**RAS \_ 埠 \_ 統計**](ras-port-statistics-str.md)結構，其中包含埠上目前連接（如果有的話）的各種統計資料計數器。</span><span class="sxs-lookup"><span data-stu-id="1321b-119">The [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function also returns a [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure that contains various statistic counters for the current connection, if any, on the port.</span></span> <span data-ttu-id="1321b-120">針對屬於多重連結連線的通訊埠， **RasAdminPortGetInfo** 會傳回與連接相關之所有埠的個別埠和累計統計資料的統計資料。</span><span class="sxs-lookup"><span data-stu-id="1321b-120">For a port that is part of a multilink connection, **RasAdminPortGetInfo** returns statistics for the individual port and cumulative statistics for all ports involved in the connection.</span></span> <span data-ttu-id="1321b-121">您可以使用 [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) 函數來重設埠的統計資料計數器。</span><span class="sxs-lookup"><span data-stu-id="1321b-121">You can use the [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) function to reset the statistic counters for the port.</span></span> <span data-ttu-id="1321b-122">[**RasAdminPortDisconnect**](rasadminportdisconnect.md)函式會中斷使用中的埠。</span><span class="sxs-lookup"><span data-stu-id="1321b-122">The [**RasAdminPortDisconnect**](rasadminportdisconnect.md) function disconnects a port that is in use.</span></span>

<span data-ttu-id="1321b-123">您可以使用 [**RasAdminFreeBuffer**](rasadminfreebuffer.md) 函式來釋放 [**RasAdminPortEnum**](rasadminportenum.md) 和 [**RasAdminPortGetInfo**](rasadminportgetinfo.md) 函式所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1321b-123">Use the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function to free memory allocated by the [**RasAdminPortEnum**](rasadminportenum.md) and [**RasAdminPortGetInfo**](rasadminportgetinfo.md) functions.</span></span> <span data-ttu-id="1321b-124">您可以使用 [**RasAdminGetErrorString**](rasadmingeterrorstring.md) 函式來取得字串，此字串描述其中一個 ras 伺服器管理 (RasAdmin) 函式所傳回的 ras 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1321b-124">Use the [**RasAdminGetErrorString**](rasadmingeterrorstring.md) function to get a string that describes a RAS error code returned by one of the RAS server administration (RasAdmin) functions.</span></span>

 

 





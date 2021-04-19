---
description: NSPGetServiceClassInfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: SPI 中的 Helper 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970991"
---
# <a name="helper-functions-in-the-spi"></a><span data-ttu-id="4d6bd-103">SPI 中的 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="4d6bd-103">Helper Functions in the SPI</span></span>

-   [<span data-ttu-id="4d6bd-104">**NSPGetServiceClassInfo**</span><span class="sxs-lookup"><span data-stu-id="4d6bd-104">**NSPGetServiceClassInfo**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

<span data-ttu-id="4d6bd-105">[**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)函式會抓取命名空間提供者已保留的服務類別架構資訊。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-105">The [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) function retrieves service class schema information that has been retained by a namespace provider.</span></span> <span data-ttu-id="4d6bd-106">Windows 通訊端 2 DLL 也會在其實 [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)中使用它。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-106">It is also used by the Windows Sockets 2 DLL in its implementation of [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span></span>

<span data-ttu-id="4d6bd-107">下列巨集定義于 *Svcguid .h* 標頭檔中，可協助在已知的服務類別與這些命名空間之間進行對應。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-107">The following macros defined in the *Svcguid.h* header file and can aid in mapping between well known service classes and these namespaces.</span></span>

| <span data-ttu-id="4d6bd-108">巨集名稱</span><span class="sxs-lookup"><span data-stu-id="4d6bd-108">Macro name</span></span>                                                                              | <span data-ttu-id="4d6bd-109">Description</span><span class="sxs-lookup"><span data-stu-id="4d6bd-109">Description</span></span>                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d6bd-110">**SVCID \_ TCP (埠)**</span><span class="sxs-lookup"><span data-stu-id="4d6bd-110">**SVCID\_TCP(Port)**</span></span><br/> <span data-ttu-id="4d6bd-111">**SVCID \_ UDP (埠)**</span><span class="sxs-lookup"><span data-stu-id="4d6bd-111">**SVCID\_UDP(Port)**</span></span><br/>                         | <span data-ttu-id="4d6bd-112">如果是網際網路通訊協定的 TCP 或 UDP 埠，則會傳回 GUID。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-112">Given a TCP or UDP port for the Internet protocol, returns the GUID.</span></span>                                                                               |
| <span data-ttu-id="4d6bd-113">**為 \_ SVCID \_ TCP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="4d6bd-113">**IS\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="4d6bd-114">**是 \_ SVCID \_ UDP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="4d6bd-114">**IS\_SVCID\_UDP(GUID)**</span></span><br/>                 | <span data-ttu-id="4d6bd-115">如果 TCP 或 UDP 的 GUID 在允許的範圍內，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-115">Returns **TRUE** if the GUID for TCP or UDP is within the allowable range.</span></span>                                                                         |
| <span data-ttu-id="4d6bd-116">**\_從 \_ SVCID \_ TCP (GUID 的埠)**</span><span class="sxs-lookup"><span data-stu-id="4d6bd-116">**PORT\_FROM\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="4d6bd-117">**埠 \_ 從 \_ SVCID \_ UDP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="4d6bd-117">**PORT\_FROM\_SVCID\_UDP(GUID)**</span></span><br/> | <span data-ttu-id="4d6bd-118">傳回與 GUID 相關聯的 TCP 或 UDP 埠。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-118">Returns the TCP or UDP port associated with the GUID.</span></span>                                                                                              |
| <span data-ttu-id="4d6bd-119">**SVCID \_ NETWARE (SAPID)**</span><span class="sxs-lookup"><span data-stu-id="4d6bd-119">**SVCID\_NETWARE(SAPID)**</span></span><br/>                                                    | <span data-ttu-id="4d6bd-120">假設服務廣告通訊協定 (SAP) 識別碼，則會傳回 GUID。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-120">Given the Service Advertising Protocol (SAP) identifier, returns the GUID.</span></span> <span data-ttu-id="4d6bd-121">此宏會搭配 NetWare 環境內的 SAP 命名空間使用。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-121">This macro is used with the SAP namespace within a NetWare environment.</span></span> |
| <span data-ttu-id="4d6bd-122">**\_從 \_ SVCID \_ NETWARE (GUID) SAPID**</span><span class="sxs-lookup"><span data-stu-id="4d6bd-122">**SAPID\_FROM\_SVCID\_NETWARE(GUID)**</span></span><br/>                                        | <span data-ttu-id="4d6bd-123">傳回與 GUID 相關聯的 NetWare SAP 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-123">Returns the NetWare SAP identifier associated with the GUID.</span></span> <span data-ttu-id="4d6bd-124">此宏會搭配 NetWare 環境內的 SAP 命名空間使用。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-124">This macro is used with the SAP namespace within a NetWare environment.</span></span>               |
| <span data-ttu-id="4d6bd-125">**是 \_ SVCID \_ NETWARE (GUID)**</span><span class="sxs-lookup"><span data-stu-id="4d6bd-125">**IS\_SVCID\_NETWARE(GUID)**</span></span><br/>                                                 | <span data-ttu-id="4d6bd-126">如果適用于 NetWare 的 GUID 位於允許的範圍內，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-126">Returns **TRUE** if the GUID for NetWare is within the allowable range.</span></span> <span data-ttu-id="4d6bd-127">此宏會搭配 NetWare 環境內的 SAP 命名空間使用。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-127">This macro is used with the SAP namespace within a NetWare environment.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="4d6bd-128">*Svcguid* 標頭檔不會自動包含在 *Winsock2* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="4d6bd-128">The *Svcguid.h* header file is not automatically included by the *Winsock2.h* header file.</span></span>

 

 

 





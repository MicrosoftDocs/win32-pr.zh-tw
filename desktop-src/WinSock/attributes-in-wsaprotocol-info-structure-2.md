---
description: XP1 \_ 支援 \_ \_ \_ \_ Winsock WSAPROTOCOL 資訊結構中的 multipoint、XP1 multipoint 控制項平面和 XP1 \_ multipoint \_ 資料 \_ 平面屬性參數 \_ 。
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: WSAPROTOCOL_INFO 結構中的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39ea2905da3228860d4fe22f5a0f0d954ce0624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973273"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a><span data-ttu-id="87933-103">WSAPROTOCOL 資訊結構中的屬性 \_</span><span class="sxs-lookup"><span data-stu-id="87933-103">Attributes in WSAPROTOCOL\_INFO Structure</span></span>

<span data-ttu-id="87933-104">為了支援上述分類法， [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構中的三個屬性參數可分別用來區分控制項和資料平面中使用的配置：</span><span class="sxs-lookup"><span data-stu-id="87933-104">In support of the taxonomy described above, three attribute parameters in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure are used to distinguish the schemes used in the control and data planes respectively:</span></span>

-   <span data-ttu-id="87933-105">XP1 \_ 支援 \_ multipoint 值為1的 multipoint 表示此通訊協定專案支援 multipoint 通訊，且下列兩個參數有意義。</span><span class="sxs-lookup"><span data-stu-id="87933-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="87933-106">XP1 \_ MULTIPOINT \_ 控制 \_ 平面會指出控制平面的根目錄 (值 = 1) 或 nonrooted (值 = 0) 。</span><span class="sxs-lookup"><span data-stu-id="87933-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="87933-107">XP1 \_ MULTIPOINT \_ 資料 \_ 平面會指出資料平面是否為 root (value = 1) 或 nonrooted (value = 0) 。</span><span class="sxs-lookup"><span data-stu-id="87933-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="87933-108">請注意，如果 multipoint 通訊協定支援 root 和 nonrooted 資料平面（每個都有一個專案），就會出現兩個 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案。</span><span class="sxs-lookup"><span data-stu-id="87933-108">Note that two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

<span data-ttu-id="87933-109">應用程式可以使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) 來探索指定的通訊協定是否支援 multipoint 通訊，如果是，則分別支援控制和資料平面的方式。</span><span class="sxs-lookup"><span data-stu-id="87933-109">The application can use [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) to discover whether multipoint communications is supported for a given protocol and, if so, how it is supported with respect to the control and data planes, respectively.</span></span>

 

 

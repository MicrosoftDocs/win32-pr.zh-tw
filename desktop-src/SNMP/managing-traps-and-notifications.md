---
title: 管理陷阱和通知
description: 您必須透過呼叫 SnmpRegister 函式和 SNMPAPI ON，以將 WinSNMP 應用程式註冊以接收陷阱和通知 \_ 。 應用程式可以呼叫 SNMPAPI OFF 的函式，以取消註冊並停用陷阱和通知 \_ 。
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840516"
---
# <a name="managing-traps-and-notifications"></a><span data-ttu-id="1b484-104">管理陷阱和通知</span><span class="sxs-lookup"><span data-stu-id="1b484-104">Managing Traps and Notifications</span></span>

<span data-ttu-id="1b484-105">您必須透過呼叫 [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) 函式和 SNMPAPI ON，以將 WinSNMP 應用程式註冊以接收陷阱和通知 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1b484-105">The WinSNMP application must register to receive traps and notifications by calling the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) function with SNMPAPI\_ON.</span></span> <span data-ttu-id="1b484-106">應用程式可以呼叫 SNMPAPI OFF 的函式，以取消註冊並停用陷阱和通知 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1b484-106">The application can unregister and disable traps and notifications by calling the function with SNMPAPI\_OFF.</span></span>

<span data-ttu-id="1b484-107">當應用程式呼叫 **SnmpRegister** 時，有數個選項可供使用。</span><span class="sxs-lookup"><span data-stu-id="1b484-107">Several options are available when the application calls **SnmpRegister**.</span></span> <span data-ttu-id="1b484-108">應用程式可以註冊或取消註冊下列陷阱和通知：</span><span class="sxs-lookup"><span data-stu-id="1b484-108">The application can register or unregister for the following traps and notifications:</span></span>

-   <span data-ttu-id="1b484-109">一種陷阱或通知</span><span class="sxs-lookup"><span data-stu-id="1b484-109">One type of trap or notification</span></span>
-   <span data-ttu-id="1b484-110">所有陷阱和通知</span><span class="sxs-lookup"><span data-stu-id="1b484-110">All traps and notifications</span></span>
-   <span data-ttu-id="1b484-111">所有陷阱和通知要求的來源</span><span class="sxs-lookup"><span data-stu-id="1b484-111">All sources of trap and notification requests</span></span>
-   <span data-ttu-id="1b484-112">所有管理實體的陷阱和通知</span><span class="sxs-lookup"><span data-stu-id="1b484-112">Traps and notifications from all management entities</span></span>
-   <span data-ttu-id="1b484-113">每個內容的陷阱和通知</span><span class="sxs-lookup"><span data-stu-id="1b484-113">Traps and notifications for every context</span></span>

<span data-ttu-id="1b484-114">若要註冊並收到預先定義的陷阱或通知型別，應用程式必須針對每個預先定義的類型，定義一個 ([**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 結構) 的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="1b484-114">To register and receive a predefined trap or notification type, the application must define an object identifier (an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure) for each predefined type.</span></span> <span data-ttu-id="1b484-115">此結構必須包含陷阱或通知類型的模式比對順序。</span><span class="sxs-lookup"><span data-stu-id="1b484-115">The structure must contain a pattern-matching sequence for the type of trap or notification.</span></span> <span data-ttu-id="1b484-116">RFC 1907：「簡易網路管理通訊協定第2版 (SNMPv2) 的管理資訊基礎」會定義陷阱和通知物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="1b484-116">RFC 1907, "Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)," defines trap and notification object identifiers.</span></span>

<span data-ttu-id="1b484-117">若要取出 WinSNMP 會話的未完成陷阱資料和通知，必須使用 [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)函式所傳回的會話控制碼來呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)函數。</span><span class="sxs-lookup"><span data-stu-id="1b484-117">To retrieve outstanding trap data and notifications for a WinSNMP session, a WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function with the session handle returned by the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span>

<span data-ttu-id="1b484-118">如需詳細資訊，請參閱傳送 [Snmp 訊息](sending-snmp-messages.md) 和 [接收 snmp 訊息](receiving-snmp-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="1b484-118">For more information, see [Sending SNMP Messages](sending-snmp-messages.md) and [Receiving SNMP Messages](receiving-snmp-messages.md).</span></span> <span data-ttu-id="1b484-119">如需有關配置和解除配置陷阱和通知資源的詳細資訊，請參閱配置 [WinSNMP 記憶體物件](allocating-winsnmp-memory-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="1b484-119">For additional information about allocation and deallocation of resources for traps and notifications, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 





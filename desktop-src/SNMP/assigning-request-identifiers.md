---
title: 指派要求識別碼
description: WinSNMP 應用程式可以呼叫 SnmpCreatePdu 函式或 SnmpSetPduData 函數，將應用程式產生的要求識別碼指派給 PDU。 應用程式必須傳遞要求識別碼參數中的值 \_ 。
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f0ec1f5f3ca4347b6344aa111b91e735f06ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671079"
---
# <a name="assigning-request-identifiers"></a><span data-ttu-id="243ca-104">指派要求識別碼</span><span class="sxs-lookup"><span data-stu-id="243ca-104">Assigning Request Identifiers</span></span>

<span data-ttu-id="243ca-105">WinSNMP 應用程式可以呼叫 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 函式或 [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) 函數，將應用程式產生的要求識別碼指派給 PDU。</span><span class="sxs-lookup"><span data-stu-id="243ca-105">A WinSNMP application can call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function to assign an application-generated request identifier to a PDU.</span></span> <span data-ttu-id="243ca-106">應用程式必須傳遞 *要求 \_ 識別碼* 參數中的值。</span><span class="sxs-lookup"><span data-stu-id="243ca-106">The application must pass the value in the *request\_id* parameter.</span></span>

<span data-ttu-id="243ca-107">應用程式可以藉由在 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)函式的 *request \_ id* 參數中傳遞零，要求 Microsoft WinSNMP 執行產生並將要求識別碼指派給 PDU。</span><span class="sxs-lookup"><span data-stu-id="243ca-107">An application can request that the Microsoft WinSNMP implementation generate and assign a request identifier to a PDU by passing zero in the *request\_id* parameter of the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="243ca-108">應用程式可以透過呼叫 [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) 函式來取得指派的要求識別碼。</span><span class="sxs-lookup"><span data-stu-id="243ca-108">The application can retrieve the assigned request identifier with a call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function.</span></span>

<span data-ttu-id="243ca-109">若要指派等於特定值（包括零）的要求識別碼，應用程式必須在 [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)函數的 *request \_ id* 參數中傳遞該值。</span><span class="sxs-lookup"><span data-stu-id="243ca-109">To assign a request identifier equal to a specific value, including zero, the application must pass that value in the *request\_id* parameter of the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span>

<span data-ttu-id="243ca-110">當執行執行應用程式的重新傳輸原則時，它會在每個重新傳輸的 SNMP 訊息中包含原始 PDU 的 **要求 \_ 識別碼** 欄位。</span><span class="sxs-lookup"><span data-stu-id="243ca-110">When the implementation executes the application's retransmission policy, it includes the **request\_id** field of the original PDU in each retransmitted SNMP message.</span></span> <span data-ttu-id="243ca-111">如需詳細資訊，請參閱 [關於重新傳輸](about-retransmission.md) 和 [管理重新傳輸原則](managing-the-retransmission-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="243ca-111">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

> [!Note]  
> <span data-ttu-id="243ca-112">當實值從 SNMPv1 實體收到陷阱時，它會將非零值指派給 PDU 的 **要求 \_ 識別碼** 欄位。</span><span class="sxs-lookup"><span data-stu-id="243ca-112">When the implementation receives traps from an SNMPv1 entity, it assigns a non-zero value to the **request\_id** field of the PDU.</span></span> <span data-ttu-id="243ca-113">此值可能會複製應用程式在要求 PDU 中所使用的要求識別碼。</span><span class="sxs-lookup"><span data-stu-id="243ca-113">This value may duplicate a request identifier used by the application in a request PDU.</span></span> <span data-ttu-id="243ca-114">應用程式必須檢查是否有重複。</span><span class="sxs-lookup"><span data-stu-id="243ca-114">Applications must check for duplication.</span></span>

 

 

 





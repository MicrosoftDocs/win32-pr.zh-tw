---
title: 使用通訊協定資料單位
description: 簡易網路管理通訊協定 (SNMP) 以 SNMP 訊息的形式傳送作業要求和回應。
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- 使用通訊協定資料單位 SNMP
- 通訊協定資料單位 SNMP，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021767"
---
# <a name="working-with-protocol-data-units"></a><span data-ttu-id="987f6-105">使用通訊協定資料單位</span><span class="sxs-lookup"><span data-stu-id="987f6-105">Working with Protocol Data Units</span></span>

<span data-ttu-id="987f6-106">簡易網路管理通訊協定 (SNMP) 以 SNMP 訊息的形式傳送作業要求和回應。</span><span class="sxs-lookup"><span data-stu-id="987f6-106">The Simple Network Management Protocol (SNMP) sends operation requests and responses as SNMP messages.</span></span> <span data-ttu-id="987f6-107">SNMP 訊息是 SNMP 通訊協定資料單位 (PDU) 再加上相關 RFC 所定義的其他訊息標頭元素。</span><span class="sxs-lookup"><span data-stu-id="987f6-107">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="987f6-108">PDU 包含變數系結清單。</span><span class="sxs-lookup"><span data-stu-id="987f6-108">A PDU includes a variable binding list.</span></span>

<span data-ttu-id="987f6-109">PDU 的結構受限於 Microsoft 的 WinSNMP 實行。</span><span class="sxs-lookup"><span data-stu-id="987f6-109">The structure of a PDU is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="987f6-110">WinSNMP 應用程式可以存取具有類型 **HSNMP \_ pdu** 之控制碼的 PDU。</span><span class="sxs-lookup"><span data-stu-id="987f6-110">A WinSNMP application can access a PDU with a handle of the type **HSNMP\_PDU**.</span></span> <span data-ttu-id="987f6-111">WinSNMP 應用程式必須先建立 PDU，然後才能呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式或 [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) 函式。</span><span class="sxs-lookup"><span data-stu-id="987f6-111">The WinSNMP application must create a PDU before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function or the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function.</span></span>

<span data-ttu-id="987f6-112">應用程式可以解壓縮和更新 PDU 的資料元素，以及釋放配置給 Pdu 的資源。</span><span class="sxs-lookup"><span data-stu-id="987f6-112">The application can extract and update the data elements of a PDU, and release resources allocated for PDUs.</span></span> <span data-ttu-id="987f6-113">若要執行這些作業，應用程式會使用 WinSNMP [PDU 功能](winsnmp-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="987f6-113">To perform these operations, the application uses the WinSNMP [PDU functions](winsnmp-functions.md).</span></span> <span data-ttu-id="987f6-114">下表列出的主題將討論如何在 WinSNMP 程式設計環境中使用 Pdu。</span><span class="sxs-lookup"><span data-stu-id="987f6-114">The following table lists topics that discuss working with PDUs in the WinSNMP programming environment.</span></span>



| <span data-ttu-id="987f6-115">主題</span><span class="sxs-lookup"><span data-stu-id="987f6-115">Topic</span></span>                                                                        | <span data-ttu-id="987f6-116">描述</span><span class="sxs-lookup"><span data-stu-id="987f6-116">Description</span></span>                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="987f6-117">建立 PDU</span><span class="sxs-lookup"><span data-stu-id="987f6-117">Creating a PDU</span></span>](creating-a-pdu.md)                                         | <span data-ttu-id="987f6-118">說明如何建立 PDU。</span><span class="sxs-lookup"><span data-stu-id="987f6-118">Describes how to create a PDU.</span></span>                                     |
| [<span data-ttu-id="987f6-119">更新 PDU</span><span class="sxs-lookup"><span data-stu-id="987f6-119">Updating a PDU</span></span>](updating-a-pdu.md)                                         | <span data-ttu-id="987f6-120">說明如何取出和更新 PDU 欄位。</span><span class="sxs-lookup"><span data-stu-id="987f6-120">Describes how to retrieve and update PDU fields.</span></span>                   |
| [<span data-ttu-id="987f6-121">複製 PDU</span><span class="sxs-lookup"><span data-stu-id="987f6-121">Duplicating a PDU</span></span>](duplicating-a-pdu.md)                                   | <span data-ttu-id="987f6-122">說明如何複製 PDU。</span><span class="sxs-lookup"><span data-stu-id="987f6-122">Describes how to duplicate a PDU.</span></span>                                  |
| [<span data-ttu-id="987f6-123">驗證 PDU</span><span class="sxs-lookup"><span data-stu-id="987f6-123">Validating a PDU</span></span>](validating-a-pdu.md)                                     | <span data-ttu-id="987f6-124">描述 PDU 的驗證。</span><span class="sxs-lookup"><span data-stu-id="987f6-124">Describes the validation of a PDU.</span></span>                                 |
| [<span data-ttu-id="987f6-125">符合回應和要求 Pdu</span><span class="sxs-lookup"><span data-stu-id="987f6-125">Matching Response and Request PDUs</span></span>](matching-response-and-request-pdus.md) | <span data-ttu-id="987f6-126">描述將回應 PDU 與要求 PDU 進行比對的程式。</span><span class="sxs-lookup"><span data-stu-id="987f6-126">Describes the process of matching a response PDU to a request PDU.</span></span> |



 

<span data-ttu-id="987f6-127">如需詳細資訊，請參閱 [使用變數](working-with-variable-binding-lists.md) 系結清單和 [資源控制碼物件](resource-handle-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="987f6-127">For more information, see [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Resource Handle Objects](resource-handle-objects.md).</span></span>

 

 





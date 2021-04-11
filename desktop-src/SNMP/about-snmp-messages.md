---
title: 關於 SNMP 訊息
description: 簡易網路管理通訊協定會使用訊息來進行通訊，並在遠端 SNMP 實體之間交換資訊。
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0426bf44d976ddf9e2eafe2093dcea94956cb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371996"
---
# <a name="about-snmp-messages"></a><span data-ttu-id="8b9ba-103">關於 SNMP 訊息</span><span class="sxs-lookup"><span data-stu-id="8b9ba-103">About SNMP Messages</span></span>

<span data-ttu-id="8b9ba-104">簡易網路管理通訊協定會使用訊息來進行通訊，並在遠端 SNMP 實體之間交換資訊。</span><span class="sxs-lookup"><span data-stu-id="8b9ba-104">The Simple Network Management Protocol uses messages to communicate and exchange information between remote SNMP entities.</span></span> <span data-ttu-id="8b9ba-105">SNMP 訊息包含通訊協定資料單位 (的 Pdu) 再加上相關 RFC 所定義的其他訊息標頭元素。</span><span class="sxs-lookup"><span data-stu-id="8b9ba-105">SNMP messages contain protocol data units (PDUs) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="8b9ba-106">PDU 是包含 SNMP 資料元件 (或欄位) 的資料封包。</span><span class="sxs-lookup"><span data-stu-id="8b9ba-106">A PDU is a data packet that contains SNMP data components (or fields).</span></span>

<span data-ttu-id="8b9ba-107">SNMPv1 和 SNMPv2C 的 SNMP 訊息格式都相同。</span><span class="sxs-lookup"><span data-stu-id="8b9ba-107">The format of an SNMP message is the same for both SNMPv1 and SNMPv2C.</span></span> <span data-ttu-id="8b9ba-108">不過，SNMPv2C 支援額外的 PDU 類型。</span><span class="sxs-lookup"><span data-stu-id="8b9ba-108">However, SNMPv2C supports additional PDU types.</span></span> <span data-ttu-id="8b9ba-109">例如，它支援 [SNMP \_ PDU \_ GETBULK](snmp-variable-types-and-request-pdu-types.md) 要求類型，可讓應用程式有效率地從目標實體中取出大型資料區塊。</span><span class="sxs-lookup"><span data-stu-id="8b9ba-109">For example, it supports the [SNMP\_PDU\_GETBULK](snmp-variable-types-and-request-pdu-types.md) request type, which enables an application to efficiently retrieve large blocks of data from target entities.</span></span>

 

 





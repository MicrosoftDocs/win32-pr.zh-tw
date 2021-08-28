---
title: 使用通訊協定資料單位
description: 簡易網路管理通訊協定 (SNMP) 以 SNMP 訊息的形式傳送作業要求和回應。
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- 使用通訊協定資料單位 SNMP
- 通訊協定資料單位 SNMP，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61fff4aed06d548718df130801c5c64674ff0b10feaf52b8bfad208d441d4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142761"
---
# <a name="working-with-protocol-data-units"></a>使用通訊協定資料單位

簡易網路管理通訊協定 (SNMP) 以 SNMP 訊息的形式傳送作業要求和回應。 SNMP 訊息是 SNMP 通訊協定資料單位 (PDU) 再加上相關 RFC 所定義的其他訊息標頭元素。 PDU 包含變數系結清單。

PDU 的結構受限於 Microsoft 的 WinSNMP 實行。 WinSNMP 應用程式可以存取具有類型 **HSNMP \_ pdu** 之控制碼的 PDU。 WinSNMP 應用程式必須先建立 PDU，然後才能呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式或 [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) 函式。

應用程式可以解壓縮和更新 PDU 的資料元素，以及釋放配置給 Pdu 的資源。 若要執行這些作業，應用程式會使用 WinSNMP [PDU 功能](winsnmp-functions.md)。 下表列出的主題將討論如何在 WinSNMP 程式設計環境中使用 Pdu。



| 主題                                                                        | 描述                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [建立 PDU](creating-a-pdu.md)                                         | 說明如何建立 PDU。                                     |
| [更新 PDU](updating-a-pdu.md)                                         | 說明如何取出和更新 PDU 欄位。                   |
| [複製 PDU](duplicating-a-pdu.md)                                   | 說明如何複製 PDU。                                  |
| [驗證 PDU](validating-a-pdu.md)                                     | 描述 PDU 的驗證。                                 |
| [符合回應和要求 Pdu](matching-response-and-request-pdus.md) | 描述將回應 PDU 與要求 PDU 進行比對的程式。 |



 

如需詳細資訊，請參閱 [使用變數](working-with-variable-binding-lists.md) 系結清單和 [資源控制碼物件](resource-handle-objects.md)。

 

 





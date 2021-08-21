---
title: 管理陷阱和通知
description: 您必須透過呼叫 SnmpRegister 函式和 SNMPAPI ON，以將 WinSNMP 應用程式註冊以接收陷阱和通知 \_ 。 應用程式可以呼叫 SNMPAPI OFF 的函式，以取消註冊並停用陷阱和通知 \_ 。
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402a768aa28efb6f2fdc18994d749cfca2f2c412f748f853fb76fcd7fe3e41d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009376"
---
# <a name="managing-traps-and-notifications"></a>管理陷阱和通知

您必須透過呼叫 [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) 函式和 SNMPAPI ON，以將 WinSNMP 應用程式註冊以接收陷阱和通知 \_ 。 應用程式可以呼叫 SNMPAPI OFF 的函式，以取消註冊並停用陷阱和通知 \_ 。

當應用程式呼叫 **SnmpRegister** 時，有數個選項可供使用。 應用程式可以註冊或取消註冊下列陷阱和通知：

-   一種陷阱或通知
-   所有陷阱和通知
-   所有陷阱和通知要求的來源
-   所有管理實體的陷阱和通知
-   每個內容的陷阱和通知

若要註冊並收到預先定義的陷阱或通知型別，應用程式必須針對每個預先定義的類型，定義一個 ([**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 結構) 的物件識別碼。 此結構必須包含陷阱或通知類型的模式比對順序。 RFC 1907：「簡易網路管理通訊協定第2版 (SNMPv2) 的管理資訊基礎」會定義陷阱和通知物件識別碼。

若要取出 WinSNMP 會話的未完成陷阱資料和通知，必須使用 [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)函式所傳回的會話控制碼來呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)函數。

如需詳細資訊，請參閱傳送 [Snmp 訊息](sending-snmp-messages.md) 和 [接收 snmp 訊息](receiving-snmp-messages.md)。 如需有關配置和解除配置陷阱和通知資源的詳細資訊，請參閱配置 [WinSNMP 記憶體物件](allocating-winsnmp-memory-objects.md)。

 

 





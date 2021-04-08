---
title: 更新 PDU
description: 藉由使用 SnmpGetPduData 和 SnmpSetPduData 函式，WinSNMP 應用程式可以取出和更新選取的 PDU 欄位。
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675091"
---
# <a name="updating-a-pdu"></a>更新 PDU

藉由使用 [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) 和 [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) 函式，WinSNMP 應用程式可以取出和更新選取的 PDU 欄位。

應用程式可以從特定的 PDU 取出 PDU 類型、要求識別碼、錯誤狀態和錯誤索引欄位。 它也可以取出變數系結清單的控制碼。 應用程式可以更新 [ **PDU \_ 類型** ] 和 [ **要求 \_ 識別碼** ] 欄位。

如果 PDU 類型等於 SNMP \_ PDU \_ GETBULK，則應用程式也可以更新 PDU 的 **非 \_ 中繼器** 和 **max \_ 重複** 欄位。

 

 





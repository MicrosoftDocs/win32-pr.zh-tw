---
title: 驗證 PDU
description: 當 WinSNMP 應用程式呼叫 SnmpSendMsg 函式或 SnmpEncodeMsg 函式時，Microsoft 的 WinSNMP 實行會確認 PDU 和其他函式參數的有效性。
ms.assetid: 0f5754ff-3688-465b-a1ad-bf7d89d7dbd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d3fe0f9831f285b51b3060517d2037a8ec05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372468"
---
# <a name="validating-a-pdu"></a>驗證 PDU

當 WinSNMP 應用程式呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式或 [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) 函式時，Microsoft 的 WINSNMP 實行會確認 PDU 和其他函式參數的有效性。

一個 PDU 資料元件的值 (或欄位) 可以個別有效，但可能與其他欄位的值組合無效。 例如，除非 PDU 的 **pdu \_ 類型** 欄位是 snmp \_ pdu \_ GETBULK 或 snmp \_ pdu \_ 回應，否則 **錯誤 \_ 狀態** 和 **錯誤 \_ 索引** 欄位都必須等於零。 任何其他的值組合都會構成不正確 PDU。

此執行會拒絕不正確 Pdu，並傳回錯誤狀態 SNMPAPI \_ 失敗。 它會設定等於 SNMPAPI PDU 不正確擴充 \_ 錯誤碼 \_ 。

 

 





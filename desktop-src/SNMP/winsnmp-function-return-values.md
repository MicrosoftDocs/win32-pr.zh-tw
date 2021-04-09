---
title: WinSNMP 函數傳回值
description: 來自 WinSNMP 函式呼叫的傳回值可以是 Microsoft WinSNMP 執行為 WinSNMP 應用程式佈建之資源的控制碼。
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023970"
---
# <a name="winsnmp-function-return-values"></a>WinSNMP 函數傳回值

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]

來自 WinSNMP 函式呼叫的傳回值可以是 Microsoft WinSNMP 執行為 WinSNMP 應用程式佈建之資源的控制碼。

下表列出此執行所配置的五種資源控制碼類型。



| 控制碼類型    | Description                       |
|----------------|-----------------------------------|
| HSNMP \_ 會話 | 對 WinSNMP 會話的處理       |
| HSNMP \_ 實體  | SNMP 實體的控制碼          |
| HSNMP \_ 內容 | SNMP 內容的控制碼         |
| HSNMP \_ PDU     | 通訊協定資料單位的控制碼    |
| HSNMP \_ VBL     | 變數系結清單的控制碼 |



 

如需詳細資訊，請參閱 [資源控制碼物件](resource-handle-objects.md)。

傳回值也可以是代表 SNMPAPI 狀態值之 **smiUINT32** 類型的不帶正負號長整數值 \_ 。

下表列出的是 WinSNMP 狀態值及其意義。



| 狀態           | 描述                                                                      |
|------------------|----------------------------------------------------------------------------------|
| SNMPAPI \_ 失敗 | 表示發生錯誤。 等於0或 **Null**。                                    |
| SNMPAPI \_ 成功 | 表示函式已順利完成。 等於1或正計數。 |



 

 

 
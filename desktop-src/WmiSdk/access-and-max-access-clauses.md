---
description: 每個 MIB 物件定義都包含存取 (SNMPv1) 或 MAX 存取 (SNMPv2C) 子句，可定義物件的存取權限。
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: 存取和最大存取權子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978256"
---
# <a name="access-and-max-access-clauses"></a>存取和最大存取權子句

每個 MIB 物件定義都包含存取 (SNMPv1) 或 MAX 存取 (SNMPv2C) 子句，可定義物件的存取權限。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

下表列出 SNMPv1 存取子句的對應。



| MIB 存取子句 | CIM 辨識符號       |
|-------------------|---------------------|
| 唯讀         | **讀取**            |
| 讀寫        | **讀取**、 **寫入** |
| 唯寫        | **寫入**           |
| 無法存取    | **無法 \_ 存取** |



 

下表列出 SNMPv2C MAX ACCESS 子句的對應。



| MIB-存取子句     | CIM 辨識符號       |
|-----------------------|---------------------|
| 唯讀             | **讀取**            |
| 讀寫            | **讀取**、 **寫入** |
| 讀取-建立           | **讀取**            |
| 可存取-通知 | **無法 \_ 存取** |
| 無法存取        | **無法 \_ 存取** |



 

當 MIB 物件對應到無法存取的，而且不是類別的索引鍵屬性時，就不會有 MIB 物件本身的對應。

 

 




---
title: 使用變數系結清單
description: 變數系結是 SNMP 物件實例名稱與關聯值的配對。 變數系結清單是一系列的變數系結專案。 在 WinSNMP 中，通訊協定資料單位 (PDU) 包含變數系結清單。
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- 使用變數系結清單 SNMP
- 變數系結清單 SNMP，SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103681450"
---
# <a name="working-with-variable-binding-lists"></a>使用變數系結清單

*變數* 系結是 SNMP 物件實例名稱與關聯值的配對。 變數系結 *清單* 是一系列的變數系結專案。 在 WinSNMP 中，通訊協定資料單位 (PDU) 包含變數系結清單。

變數系結清單結構的詳細資料僅限於 Microsoft 的 WinSNMP 實行。 WinSNMP 應用程式可以使用 **HSNMP \_ VBL** 類型的控制碼來存取變數系結清單。 如需詳細資訊，請參閱 [資源控制碼物件](resource-handle-objects.md)。

WinSNMP 應用程式可以建立和操作變數系結清單，並將它們包含在 Pdu 中。 若要執行這些作業，應用程式會使用 WinSNMP [變數](winsnmp-functions.md)系結函式。 如需使用 WinSNMP 和變數系結清單的詳細資訊，請參閱下表所列的主題。



| 主題                                                                    | 描述                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [建立變數系結清單](creating-a-variable-binding-list.md) | 描述如何建立變數系結清單。 |
| [管理變數系結清單](managing-a-variable-binding-list.md) | 說明如何管理變數系結清單。 |



 

如需變數系結和變數系結清單的詳細資訊，請參閱 [RFC1905](https://www.ietf.org/rfc/rfc1905.txt)「簡易網路管理通訊協定第2版的通訊協定作業 (SNMPv2) 」和「WinSNMP [變數](winsnmp-functions.md)系結函式」。

 

 





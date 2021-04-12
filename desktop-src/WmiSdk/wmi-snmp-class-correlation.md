---
description: 相互關聯會影響從 SMIR 傳回的一組類別。
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: WMI SNMP 類別相互關聯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192186"
---
# <a name="wmi-snmp-class-correlation"></a>WMI SNMP 類別相互關聯

相互關聯會影響從 SMIR 傳回的一組類別。 相互關聯的類別是指定的 SNMP 裝置在發生列舉時所能支援的類別。 Noncorrelated 列舉會傳回 SMIR 中所有出現的類別，不論裝置是否支援它們。 相互關聯是 WMI SNMP 提供者的一項功能，可以關閉或 (預設) 。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

相互關聯可能會讓您無法看到裝置實際支援的所有類別。 如果您知道特定類別受到支援，但不會出現在 SMIR 中，這可能是因為下列幾個原因所致：其中一個是相互關聯。 在寫入至有問題的裝置之前，請考慮關閉相互關聯。 不過，關閉相互關聯可能會導致裝置不支援的許多類別會出現在 SMIR 中。 此外，使用相互關聯會產生效能成本，因為會查詢裝置以查看它所支援的類別。 當相互關聯開啟時，SNMP 提供者會導致裝置支援類別的列舉，類似于執行 *mib 逐步* 解說工具的結果。

例如，網路系統管理員想要知道特定網路中所有受管理中樞的幾個重要資料片段。 目前裝置的資料庫及其支援的 Mib 已存在，因此不需要依賴裝置的相互關聯功能來提供支援的資料元素。 在此情況下，相互關聯可能會關閉。

下列範例顯示如何關閉相互關聯。


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



另一方面，另一個網路系統管理員可能會想要監視網路上的所有 UNIX 機器磁片磁碟機，但不熟悉這些機器上的 MIB 資料。 在此情況下，相互關聯會開啟。

 

 




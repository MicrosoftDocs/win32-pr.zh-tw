---
title: 配置的 WinSNMP 記憶體物件
description: 描述元、資源控制碼和 C 樣式字串是在 WinSNMP 程式設計環境中的三種記憶體物件類型。
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020774"
---
# <a name="allocating-winsnmp-memory-objects"></a>配置的 WinSNMP 記憶體物件

描述元、資源控制碼和 C 樣式字串是在 WinSNMP 程式設計環境中的三種記憶體物件類型。

物件的類型會決定 Microsoft WinSNMP 執行或 WinSNMP 應用程式是否配置並解除配置物件的記憶體。 這可減少暫存緩衝區空間的不必要配置，以及不必要的緩衝區複製。

下表摘要說明如何配置和解除配置 WinSNMP 記憶體物件的資源。



| 物件型別                                                                   | 說明                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 或 [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) 描述項 | 如果 WinSNMP 應用程式佈建記憶體，則必須呼叫適當的函式來解除配置記憶體。 如果執行配置記憶體，則應用程式必須呼叫 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) 函式來解除配置記憶體。 |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) 結構                                    | 如果 **值** 成員是 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 或 [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) 描述元，則應用程式必須如上面所示針對描述項繼續進行。                                                                                                     |
| 資源控制碼                                                               | 此實作為配置、管理和釋放記憶體。                                                                                                                                                                                                                         |
| C 樣式字串                                                                | WinSNMP 應用程式必須管理和釋放它所配置的記憶體。                                                                                                                                                                                                                |



 

如需詳細資訊，請參閱 [釋放 WinSNMP 描述](freeing-winsnmp-descriptors.md)項。

 

 





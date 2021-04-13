---
title: WinSNMP 描述項
description: 在 WinSNMP 程式設計環境中，描述項是下列兩個結構的其中一個。
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300280"
---
# <a name="winsnmp-descriptors"></a>WinSNMP 描述項

在 WinSNMP 程式設計環境中， *描述* 項是下列兩個結構的其中一個：

-   描述八進位字串變數的 [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) 結構
-   描述 SNMP 物件識別碼變數的 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 結構

WinSNMP 描述元是具有兩個成員的結構：長度成員、 **len** 和指標成員、 **ptr**。 **Ptr** 成員指向所需的八位字串或物件識別碼。 **Ptr** 成員可以是 **smiLPBYTE** 或 **smiLPUINT32** 資料類型。

[**SmiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)描述元或 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)描述元可以是 **smiVALUE** 結構的 **值** 成員。 [**SmiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)結構描述與變數系結專案中的變數名稱相關聯的值。

Microsoft WinSNMP 執行會為所有輸出 **smiOCTETS** 和 **smiOID** 結構配置和解除配置記憶體。 因此，應用程式必須呼叫 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) 函式，以釋放這些結構的 **ptr** 成員記憶體。

描述項中的字串成員不需要 **Null** 終止位元組。 如需管理配置給描述項之記憶體的詳細資訊，請參閱配置 [WinSNMP 記憶體物件](allocating-winsnmp-memory-objects.md)。

 

 





---
title: 管理物件識別碼
description: WinSNMP API 提供數個可簡化對 WinSNMP 應用程式之物件識別碼操作的 WinSNMP 公用程式函式。
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462408"
---
# <a name="managing-object-identifiers"></a>管理物件識別碼

WinSNMP API 提供數個可簡化對 WinSNMP 應用程式之物件識別碼操作的 [winsnmp 公用程式](winsnmp-functions.md) 函式。

[**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)函式會將物件識別碼的內部二進位標記法轉換為其點數位字串格式。 當您呼叫 [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)時，請將 MAXOBJIDSTRSIZE 長度的字串緩衝區指定 (1408 個位元組) ，以確保輸出緩衝區夠大，足以容納轉換的字串。 若要將物件識別碼從點數位字串格式轉換為其內部二進位標記法，請呼叫 [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) 函式。

若要複製 SNMP 物件識別碼，請呼叫 [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) 函數。 此函式會為新的物件識別碼配置任何必要的記憶體。

WinSNMP 應用程式必須呼叫 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)函式，以釋出針對 [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)和 [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)函數所指定之 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)結構的 **ptr** 成員所配置的資源。

[**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)函式會比較兩個 SNMP 物件識別碼。 WinSNMP 應用程式可以指定要比較的 subidentifiers 數目。 呼叫 **SnmpOidCompare** 來判斷兩個物件識別碼是否有常見的前置詞。

如需管理配置給物件識別碼之記憶體的詳細資訊，請參閱配置 [WinSNMP 記憶體物件](allocating-winsnmp-memory-objects.md)。

 

 





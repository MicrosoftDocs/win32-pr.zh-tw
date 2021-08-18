---
title: WinSNMP 結構
description: WinSNMP API 函數會使用下列結構。
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- WinSNMP 結構 SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b409b6d12063ebd3feb9c663f2d607bc5ceead0462b2945334f1e7e691c9be63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142751"
---
# <a name="winsnmp-structures"></a>WinSNMP 結構

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用[Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 Microsoft 對 ws-atomictransaction 的實。\]

WinSNMP API 函數會使用下列結構。



| 結構                                  | 描述                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | 包含代表計數器的64位不帶正負號的整數值。                                                    |
| [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | 包含變數長度的 SNMP 八位字串指標。                                                         |
| [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | 包含與指定的命名物件相關聯之 subidentifiers 的可變長度陣列指標。 |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | 表示與變數系結專案中的變數名稱相關聯的值。                              |
| [**smiVENDORINFO**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | 包含 Microsoft 的 WinSNMP 執行相關資訊。                                                    |



 

 

 
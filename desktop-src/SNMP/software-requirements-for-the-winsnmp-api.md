---
title: WinSNMP API 的軟體需求
description: WinSNMP 應用程式必須透過動態連結程式庫 WSNMP32.DLL 來存取 WinSNMP API。
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cf78c4937996a44b2a82ebeb0b2963f9a4ffaada0288068b07cd3b60432c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886068"
---
# <a name="software-requirements-for-the-winsnmp-api"></a>WinSNMP API 的軟體需求

WinSNMP 應用程式必須透過動態連結程式庫 WSNMP32.DLL 來存取 WinSNMP API。

以下是支援 WinSNMP API 功能所需的檔案。



| 檔案名稱     | 描述                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| WSNMP32.DLL.自由  | WinSNMP 程式庫                                                                              |
| WSNMP32.DLL  | 提供 WinSNMP 介面                                                                   |
| WINSNMP.H    | WinSNMP 標頭檔                                                                          |
| SNMPTRAP.EXE | 接收 SNMP 陷阱，並將其轉送至 MGMTAPI.DLL，也就是 Microsoft SNMP 管理員 API 程式庫 |
| SNMPAPI.DLL  | 提供 SNMP 公用程式                                                                      |



 

 

 





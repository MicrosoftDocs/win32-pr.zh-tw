---
title: WinSNMP API 的軟體需求
description: WinSNMP 應用程式必須透過動態連結程式庫 WSNMP32.DLL 來存取 WinSNMP API。
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182978"
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



 

 

 





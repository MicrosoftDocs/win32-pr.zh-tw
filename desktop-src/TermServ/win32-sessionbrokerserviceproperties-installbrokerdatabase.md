---
title: Win32_SessionBrokerServiceProperties 類別的 InstallBrokerDatabase 方法
description: 在中央 SQL 伺服器上安裝 RD 連線代理人資料庫。
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- InstallBrokerDatabase 方法遠端桌面服務
- InstallBrokerDatabase 方法遠端桌面服務，Win32_SessionBrokerServiceProperties 類別
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，InstallBrokerDatabase 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e77a34c70fbf06bac5501c8cacddce9feb9211d1fe21c1ef30fe429d3e75308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422448"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Win32 SessionBrokerServiceProperties 類別的 InstallBrokerDatabase 方法 \_

在中央 SQL 伺服器上安裝 RD 連線代理人資料庫。

## <a name="syntax"></a>語法


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newDbFilePath* \[在\]
</dt> <dd>

新的資料庫檔案路徑。

</dd> <dt>

*connStringToCentralDBMaster* \[在\]
</dt> <dd>

中央資料庫主資料庫的連接字串。

</dd> <dt>

*centralRdcmsDbName* \[在\]
</dt> <dd>

中央資料庫的名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






---
title: Win32_SessionBrokerServiceProperties 類別的 IsDbReachable 方法
description: 檢查資料庫是否可連線。
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- IsDbReachable 方法遠端桌面服務
- IsDbReachable 方法遠端桌面服務，Win32_SessionBrokerServiceProperties 類別
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，IsDbReachable 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1cd7aaf2035251c503d85683f9aa9e9fe7b7f6285084a97133f0573ba41d79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848415"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Win32 SessionBrokerServiceProperties 類別的 IsDbReachable 方法 \_

檢查資料庫是否可連線。

## <a name="syntax"></a>語法


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*connStringToDb* \[在\]
</dt> <dd>

資料庫的連接字串。

</dd> <dt>

*connSecondaryStringToDb* \[在\]
</dt> <dd>

中央資料庫的次要連接字串。

**Windows Server 2012 R2 和 Windows Server 2012：** 此參數在 Windows Server 2016 之前無法使用。

</dd> <dt>

*activeBrokerName* \[在\]
</dt> <dd>

Active broker 名稱。

**Windows Server 2012 R2 和 Windows Server 2012：** 此參數在 Windows Server 2016 之前無法使用。

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

 

 






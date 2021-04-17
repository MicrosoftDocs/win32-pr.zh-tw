---
title: Win32_SessionBrokerServiceProperties 類別的 SetSBDbConnectionStrings 方法
description: 將主要和次要資料庫的資料庫連接字串儲存在登錄中。
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- SetSBDbConnectionStrings 方法遠端桌面服務
- SetSBDbConnectionStrings 方法遠端桌面服務，Win32_SessionBrokerServiceProperties 類別
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，SetSBDbConnectionStrings 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4aa02cabe89e434fb8b24b308bbe2ec51fa5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465288"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Win32 SessionBrokerServiceProperties 類別的 SetSBDbConnectionStrings 方法 \_

將主要和次要資料庫的資料庫連接字串儲存在登錄中。

## <a name="syntax"></a>語法


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*connStringToCentralDBRdcms* \[在\]
</dt> <dd>

主要連接字串。

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[在\]
</dt> <dd>

次要連接字串。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                         |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






---
title: Win32_TSSessionDirectory 類別的 CreateUserDiskTemplate 方法
description: 建立使用者磁片範本。
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- CreateUserDiskTemplate 方法遠端桌面服務
- CreateUserDiskTemplate 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，CreateUserDiskTemplate 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094047"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a>Win32 TSSessionDirectory 類別的 CreateUserDiskTemplate 方法 \_

建立使用者磁片範本。

## <a name="syntax"></a>語法


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*UserDisksStorageUrl* \[在\]
</dt> <dd>

儲存所有使用者磁片之共用的位置。

</dd> <dt>

*UserDiskMaxSizeInGB* \[在\]
</dt> <dd>

所有使用者磁片的大小上限（以 gb 為單位）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 






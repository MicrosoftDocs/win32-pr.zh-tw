---
title: Win32_TSApplicationFileExtensions 類別的 FileAssociations 方法
description: 掃描登錄以取得應用程式目前的檔案關聯。
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- FileAssociations 方法遠端桌面服務
- FileAssociations 方法遠端桌面服務，Win32_TSApplicationFileExtensions 類別
- Win32_TSApplicationFileExtensions 類別遠端桌面服務，FileAssociations 方法
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45548d055d6adc90ac55e26b646abab80470297847d5daa898e63b29769dc4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737508"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a>Win32 TSApplicationFileExtensions 類別的 FileAssociations 方法 \_

掃描登錄以取得應用程式目前的檔案關聯。

## <a name="syntax"></a>語法


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AppPath* \[在\]
</dt> <dd>

指定應用程式的路徑。

</dd> <dt>

*FileAssociations* \[擴展\]
</dt> <dd>

成功完成時，會包含此應用程式的檔案關聯。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSApplicationFileExtensions**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**Win32 \_ RDFileAssociation**](win32-rdfileassociation.md)
</dt> </dl>

 

 






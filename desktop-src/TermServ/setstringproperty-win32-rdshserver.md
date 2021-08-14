---
title: 'Win32_RDSHServer 類別的 SetStringProperty 方法 (Certenroll) '
description: 更新 Win32 RDSHServer 物件的字串屬性值 \_ 。
ms.assetid: 9a338872-27fc-4e37-afd6-20a42c7859e5
ms.tgt_platform: multiple
keywords:
- SetStringProperty 方法遠端桌面服務
- SetStringProperty 方法遠端桌面服務，Win32_RDSHServer 類別
- Win32_RDSHServer 類別遠端桌面服務，SetStringProperty 方法
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2715271bcb73efd15acbef2097a29a978774e575a4fb115a9ef9e727e3efa91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349389"
---
# <a name="setstringproperty-method-of-the-win32_rdshserver-class"></a>Win32 RDSHServer 類別的 SetStringProperty 方法 \_

更新 [**Win32 \_ RDSHServer**](win32-rdshserver.md) 物件的字串屬性值。

## <a name="syntax"></a>語法


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

識別要更新之屬性的索引鍵。

</dd> <dt>

*值* \[在\]
</dt> <dd>

新的屬性值。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ CIMv2 \\ rdm<br/>                                                                |
| 標頭<br/>                   | <dl> <dt>Certenroll。h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 






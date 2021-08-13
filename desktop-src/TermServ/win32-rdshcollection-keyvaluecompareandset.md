---
title: Win32_RDSHCollection 類別的 KeyValueCompareAndSet 方法
description: 比較集合中指定的索引鍵與比較元;如果相符，索引鍵會設定為新的值。 如果索引鍵不存在，方法會將索引鍵插入集合中。
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- KeyValueCompareAndSet 方法遠端桌面服務
- KeyValueCompareAndSet 方法遠端桌面服務，Win32_RDSHCollection 類別
- Win32_RDSHCollection 類別遠端桌面服務，KeyValueCompareAndSet 方法
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52e1aaaf90313c8c1434a65c4ffd1045933ad503245f0dacbf78c2b7e1ca054a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422708"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a>Win32 RDSHCollection 類別的 KeyValueCompareAndSet 方法 \_

比較集合中指定的索引鍵與比較元;如果相符，索引鍵會設定為新的值。 如果索引鍵不存在，方法會將索引鍵插入集合中。

## <a name="syntax"></a>語法


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

要比較的索引鍵。

</dd> <dt>

*NewValue* \[在\]
</dt> <dd>

新值。

</dd> <dt>

*比較元* \[在\]
</dt> <dd>

要用來比較索引鍵的字串。

</dd> <dt>

*InitialValue* \[擴展\]
</dt> <dd>

在成功或失敗時，會包含索引鍵的起始值。

</dd> </dl>

## <a name="remarks"></a>備註

請注意，這個方法可以取出索引鍵的值，因此會封裝 [**KeyValueGet**](win32-rdshcollection-keyvalueget.md)的功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                              |
| 命名空間<br/>                | 根 \\ cimv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 






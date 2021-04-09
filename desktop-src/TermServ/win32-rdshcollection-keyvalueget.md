---
title: Win32_RDSHCollection 類別的 KeyValueGet 方法
description: 抓取與集合中指定之索引鍵相關聯的值。
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- KeyValueGet 方法遠端桌面服務
- KeyValueGet 方法遠端桌面服務，Win32_RDSHCollection 類別
- Win32_RDSHCollection 類別遠端桌面服務，KeyValueGet 方法
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5304cca379106094d4d00b9a0b5506c8df7075a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843392"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a>Win32 RDSHCollection 類別的 KeyValueGet 方法 \_

抓取與集合中指定之索引鍵相關聯的值。

## <a name="syntax"></a>語法


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

識別您想要取得之值的索引鍵。

</dd> <dt>

*值* \[擴展\]
</dt> <dd>

成功時，傳回與指定索引鍵相關聯的值。

</dd> </dl>

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

 

 






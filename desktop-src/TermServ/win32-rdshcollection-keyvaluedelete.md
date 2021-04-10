---
title: Win32_RDSHCollection 類別的 KeyValueDelete 方法
description: 從集合中刪除指定的索引鍵 (以及相關聯的值) 。
ms.assetid: 968d6744-7b4a-45e5-87fb-90c408dbc771
ms.tgt_platform: multiple
keywords:
- KeyValueDelete 方法遠端桌面服務
- KeyValueDelete 方法遠端桌面服務，Win32_RDSHCollection 類別
- Win32_RDSHCollection 類別遠端桌面服務，KeyValueDelete 方法
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueDelete
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1b4b29aea7890817c8d3cd8599f6effceb53c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934235"
---
# <a name="keyvaluedelete-method-of-the-win32_rdshcollection-class"></a>Win32 RDSHCollection 類別的 KeyValueDelete 方法 \_

從集合中刪除指定的索引鍵 (以及相關聯的值) 。

## <a name="syntax"></a>語法


```mof
uint32 KeyValueDelete(
  [in] string Key
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

要刪除的索引鍵。

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

 

 






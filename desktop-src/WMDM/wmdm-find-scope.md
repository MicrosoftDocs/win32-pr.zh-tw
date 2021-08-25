---
title: WMDM_FIND_SCOPE 列舉
description: WMDM \_ 尋找 \_ 範圍列舉型別會定義儲存物件的範圍。
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- WMDM_FIND_SCOPE 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb7d4902b1acd4223f25bdc5e8a7ca76d4495b5f465687a56b295ad2d5fbfa0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863008"
---
# <a name="wmdm_find_scope-enumeration"></a>WMDM \_ 尋找 \_ 範圍列舉

**WMDM \_ 尋找 \_ 範圍** 列舉型別會定義儲存物件的範圍。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM \_ 尋找 \_ 範圍 \_ 全域**
</dt> <dd>

在裝置上的任何位置尋找相符的物件。

</dd> <dt>

<span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM \_ 尋找 \_ 領域 \_ 直屬 \_ 子系**
</dt> <dd>

尋找此儲存體及其子系內相符的物件。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](enumeration-types.md)
</dt> </dl>

 

 






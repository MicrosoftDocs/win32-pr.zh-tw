---
description: 建立頂點著色器版本號碼權杖。
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: 'D3DVS_VERSION 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 861295c9068bee9e40174d877a78628aa405b9cfa5d46414190fbb7b37904e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527254"
---
# <a name="d3dvs_version-macro"></a>D3DVS \_ 版本宏

建立頂點著色器版本號碼權杖。

## <a name="syntax"></a>語法


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*\_主要* 
</dt> <dd>

主要頂點著色器版本。 請參閱備註以取得適當的值。

</dd> <dt>

*\_Minor* 
</dt> <dd>

次要頂點著色器版本。 請參閱備註以取得適當的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回做為頂點著色器版本的 DWORD 值。

## <a name="remarks"></a>備註

版本號碼

版本號碼是主要版本和次要頂點著色器版本號碼的組合。 有效的數位會顯示在表格中。



| 主要 | Minor | 範例             |
|-------|-------|---------------------|
| 1     | 1     | D3DVS \_ 版本 (1，1)  |
| 2     | 0     | D3DVS \_ 版本 (2，0)  |
| 3     | 0     | D3DVS \_ 版本 (3，0)  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 





---
description: 建立圖元著色器版本戳記。
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: 'D3DPS_VERSION 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322996"
---
# <a name="d3dps_version-macro"></a>D3DPS \_ 版本宏

建立圖元著色器版本戳記。

## <a name="syntax"></a>語法


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*\_主要* 
</dt> <dd>

主要圖元著色器版本。

</dd> <dt>

*\_Minor* 
</dt> <dd>

次要圖元著色器版本。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回是圖元著色器版本的 DWORD 值。

## <a name="remarks"></a>備註

版本號碼

版本號碼是主要版本和次要頂點著色器版本號碼的組合。 有效的數位會顯示在表格中。



| 主要 | Minor | 範例             |
|-------|-------|---------------------|
| 1     | 1     | D3DPS \_ 版本 (1，1)  |
| 1     | 2     | D3DPS \_ 版本 (1、2)  |
| 1     | 3     | D3DPS \_ 版本 (1，3)  |
| 1     | 4     | D3DPS \_ 版本 (1、4)  |
| 2     | 0     | D3DPS \_ 版本 (2，0)  |
| 3     | 0     | D3DPS \_ 版本 (3，0)  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DCAPS9](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 





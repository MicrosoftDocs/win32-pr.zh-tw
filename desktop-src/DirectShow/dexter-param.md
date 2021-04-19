---
description: 指定屬性在指定時間所假設的值。
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: 'DEXTER_PARAM 結構 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000411"
---
# <a name="dexter_param-structure"></a>DEXTER \_ PARAM 結構

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

指定屬性在指定時間所假設的值。

## <a name="syntax"></a>語法


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

屬性的名稱。

</dd> <dt>

**dispID**
</dt> <dd>

保留的。 設定為零。

</dd> <dt>

**\N**
</dt> <dd>

屬性所採用的值數目。

</dd> </dl>

## <a name="remarks"></a>備註

物件必須支援 **IDispatch** 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Qedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**DEXTER \_ 值**](dexter-value.md)
</dt> </dl>

 

 





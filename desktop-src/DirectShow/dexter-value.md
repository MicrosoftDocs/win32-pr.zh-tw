---
description: 識別要在轉換或效果上設定的屬性，以及屬性在轉換或效果期間所採用的相異值數目。
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: 'DEXTER_VALUE 結構 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999262"
---
# <a name="dexter_value-structure"></a>DEXTER \_ 值結構

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

識別要在轉換或效果上設定的屬性，以及屬性在轉換或效果期間所採用的相異值數目。

## <a name="syntax"></a>語法


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a>成員

<dl> <dt>

**V**
</dt> <dd>

屬性的值。

</dd> <dt>

**Rt**
</dt> <dd>

屬性假設值的時間（相對於轉換或效果的開頭）。

</dd> <dt>

**dwInterp**
</dt> <dd>

旗標，指出屬性如何從先前的值到此值之間的進展。 必須是下列其中之一：



| 值                                                                                                                                                                           | 意義                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <dt>**DEXTERF \_ 跳躍**</dt> </dl>                      | 屬性會立即跳到指定時間的新值。<br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <dt>**DEXTERF \_ 插補**</dt> </dl> | 屬性是從上一個值的一段時間內呈線性插補。<br/> |



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Qedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**DEXTER \_ 參數**](dexter-param.md)
</dt> </dl>

 

 





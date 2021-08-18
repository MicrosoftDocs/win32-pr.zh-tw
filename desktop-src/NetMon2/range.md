---
description: 範圍結構會定義有效屬性值的範圍。
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: '範圍結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0e0135a6210aebbca38bfdede00231315dd2680461f366930b24925eda830604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063718"
---
# <a name="range-structure"></a>範圍結構

**範圍** 結構會定義有效屬性值的範圍。

## <a name="syntax"></a>語法


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a>成員

<dl> <dt>

**MinValue**
</dt> <dd>

範圍中可能的最小值。

</dd> <dt>

**Timespan.maxvalue**
</dt> <dd>

範圍中最高的可能值。

</dd> </dl>

## <a name="remarks"></a>備註

**範圍** 結構是用來為通訊協定屬性指定有效的數位範圍。 如果 **PROPERTYINFO** 結構的 **DataQualifier** 成員設定為 [ **\_ QUAL \_ 範圍**]，則 [PROPERTYINFO](propertyinfo.md)結構的 **lpRange** 成員必須提供 **範圍** 結構的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 





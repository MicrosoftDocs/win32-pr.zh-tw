---
title: ErrorItem。條件
description: Condition 屬性會抓取指出錯誤條件的值。
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem 條件 Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5f4bfe2c4b2b517b0fd300a0c6465ae9f10147518937822212b621d808f0ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996638"
---
# <a name="erroritemcondition"></a>ErrorItem。條件

**Condition** 屬性會抓取指出錯誤條件的值。

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) ，代表條件碼。

## <a name="remarks"></a>備註

條件碼是 Microsoft 用來為技術支援人員提供其他資訊的值。

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ErrorItem 物件**](erroritem-object.md)
</dt> </dl>

 

 






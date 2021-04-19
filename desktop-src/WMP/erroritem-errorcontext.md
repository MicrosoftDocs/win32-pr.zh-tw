---
title: ErrorItem.errorCoNtext
description: ErrorCoNtext 屬性會抓取指出錯誤內容的值。
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- ErrorItem. errorCoNtext Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986176"
---
# <a name="erroritemerrorcontext"></a>ErrorItem.errorCoNtext

**ErrorCoNtext** 屬性會抓取指出錯誤內容的值。

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串** ，代表錯誤內容代碼。

## <a name="remarks"></a>備註

錯誤內容是 Microsoft 用來為技術支援人員提供其他資訊的資訊。

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回空字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ErrorItem 物件**](erroritem-object.md)
</dt> </dl>

 

 






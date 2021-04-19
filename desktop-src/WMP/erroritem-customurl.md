---
title: ErrorItem.customUrl
description: CustomURL 屬性會抓取網站的 URL，以顯示有關編解碼器下載失敗的特定資訊。
ms.assetid: 51028f45-2ce6-4e57-86bd-d7c2d8fb3af8
keywords:
- ErrorItem. customUrl Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.customUrl
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba285710009d03e231dcabf15f8b1e38c990026b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000459"
---
# <a name="erroritemcustomurl"></a>ErrorItem.customUrl

**CustomURL** 屬性會抓取網站的 URL，以顯示有關編解碼器下載失敗的特定資訊。

``` syntax
player.error.item(
        index
        ).customURL
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串**。

## <a name="remarks"></a>備註

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回空字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ErrorItem 物件**](erroritem-object.md)
</dt> </dl>

 

 






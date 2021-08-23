---
title: '>synconly 屬性'
description: '>synconly 屬性是布林值的字串表示，Windows Media Player 用來判斷播放清單是否僅適用于同步處理。'
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- '>synconly 屬性 Windows Media Player'
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e77fe67fe3cb943ad210f4d9beb58cfea8f32da87e6ee15955b578f07a608f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134731"
---
# <a name="synconly-attribute"></a>>synconly 屬性

**>synconly** 屬性是 **布林** 值的字串表示，Windows Media Player 用來判斷播放清單是否僅適用于同步處理。

## <a name="applies-to"></a>套用至

-   [播放清單](playlist-attributes-ref.md)

## <a name="remarks"></a>備註

值為1表示播放清單僅供同步處理使用，且不能出現在 [ **自動播放清單** ] 節點中。 值為零表示播放清單可以出現在 [ **自動播放清單** ] 節點中。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 






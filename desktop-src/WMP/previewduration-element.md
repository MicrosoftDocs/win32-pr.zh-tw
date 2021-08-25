---
title: PREVIEWDURATION 元素
description: PREVIEWDURATION 元素會定義剪輯在預覽模式中播放的時間長度。
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- PREVIEWDURATION 元素 Windows Media Player
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd01180b56816aa3458396f1c6183518d4365dce2f41643328e899057ed1ee72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862018"
---
# <a name="previewduration-element"></a>PREVIEWDURATION 元素

**PREVIEWDURATION** 元素會定義剪輯在預覽模式中播放的時間長度。

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>屬性

**值** (必要) 

剪輯在預覽模式中播放的時間長度 (以小時、分鐘、秒和百分之一為單位的) 。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                    |
|-----------------|-----------------------------|
| 父元素 | **ASX**、 **ENTRY**、 **REF** |
| 子元素  | 無                        |



 

## <a name="remarks"></a>備註

此元素定義剪輯在預覽模式中播放的時間長度。 如果這個專案出現在 **ENTRY** 元素或 **REF** 元素內，則會套用至該元素所定義的剪輯。 如果出現在 **ASX** 元素的範圍內，則會套用至中繼檔中的每個剪輯。 **REF** 元素中的 **PREVIEWDURATION** 專案優先于 ENTRY 專案中的專案，而且會優先于 **ASX** **元素中** 的 **PREVIEWDURATION** 元素。 如果未針對剪輯定義任何 **PREVIEWDURATION** 元素，則預設預覽時間為10秒。

如果剪輯有 **STARTTIME** 或 **STARTMARKER** 元素，Windows Media Player 會從下列其中一個專案所定義的點開始轉譯剪輯;否則，它會從剪輯的開頭呈現。 如果剪輯比 **PREVIEWDURATION** 元素所定義的時間短，則會正常停止。

**DURATION** 元素會覆寫 **PREVIEWDURATION** 元素。

## <a name="examples"></a>範例


```XML
<PREVIEWDURATION VALUE="0:30.0" />
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------|
| 版本<br/> | Windows Media Player 70 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 






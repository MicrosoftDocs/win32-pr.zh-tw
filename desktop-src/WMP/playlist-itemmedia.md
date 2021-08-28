---
title: 播放清單。 itemMedia
description: ItemMedia 屬性會抓取與播放清單元素中的指定索引對應的媒體物件。
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- 播放清單. itemMedia Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52b3061ef83ec246878d51528e88a12b4f10dcb3085f584a2266dc64a163b866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746862"
---
# <a name="playlistitemmedia"></a>播放清單。 itemMedia

**ItemMedia** 屬性會抓取與 **播放清單** 元素中的指定索引對應的 **媒體** 物件。

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **媒體** 物件。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*指數*
</dt> <dd>

包含播放清單專案索引的 (**長**) **數目**。

</dd> </dl>

## <a name="remarks"></a>備註

**ItemMedia** 屬性會傳回在 **播放清單** 元素中展開的媒體物件。 例如，如果播放清單中包含的三個媒體剪輯都未在 **播放清單** 元素中展開， **itemMedia** (0) 將會傳回播放清單作為媒體物件。 如果已展開播放清單， **itemMedia** (0) 將會傳回播放清單中的第一個媒體剪輯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**播放清單元素**](playlist-element.md)
</dt> </dl>

 

 






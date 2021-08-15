---
title: MediaCollection. getMediaAtom 方法
description: GetMediaAtom 方法會抓取可用屬性集合中指定的屬性所在的索引。
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- getMediaAtom 方法 Windows Media Player
- getMediaAtom 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getMediaAtom 方法
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f537b759516d5fa0f382d0c72aabbc0edb836ad8e4ae6d7f210d012fa19ea60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837201"
---
# <a name="mediacollectiongetmediaatom-method"></a>MediaCollection. getMediaAtom 方法

**GetMediaAtom** 方法會抓取可用屬性集合中指定的屬性所在的索引。

## <a name="syntax"></a>語法


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

包含屬性名稱的 **字串**。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player[屬性參考](attribute-reference.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位** (**long**) 。

## <a name="remarks"></a>備註

使用這個方法取出的索引編號可以傳遞至 *媒體*。用來存取屬性值的 **getItemInfoByAtom** 方法。 使用大型播放清單時，這項技術通常更有效率，而不是透過 *媒體* 依名稱存取屬性值。**getItemInfo** 或 *媒體*。**getItemInfoByType**。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**GetItemInfoByAtom**](media-getiteminfobyatom.md)
</dt> <dt>

[**GetItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






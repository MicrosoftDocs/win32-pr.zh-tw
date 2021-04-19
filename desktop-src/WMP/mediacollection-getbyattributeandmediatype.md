---
title: MediaCollection. getByAttributeAndMediaType 方法
description: GetByAttributeAndMediaType 方法會抓取播放清單物件，其中包含具有指定之屬性和媒體類型的媒體物件。
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- getByAttributeAndMediaType 方法 Windows Media Player
- getByAttributeAndMediaType 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getByAttributeAndMediaType 方法
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982694"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a>MediaCollection. getByAttributeAndMediaType 方法

**GetByAttributeAndMediaType** 方法會抓取 **播放清單** 物件，其中包含具有指定之屬性和媒體類型的 **媒體** 物件。

## <a name="syntax"></a>語法


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

包含屬性的 **字串**。

</dd> <dt>

*值* \[在\]
</dt> <dd>

包含值的 **字串**。

</dd> <dt>

*媒體媒體* \[在\]
</dt> <dd>

包含媒體類型的 **字串**。 必須包含下列其中一個值：「音訊」、「影片」、「相片」、「播放清單」或「其他」。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **播放清單** 物件

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> </dl>

 

 






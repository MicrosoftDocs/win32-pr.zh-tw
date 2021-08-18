---
title: StringCollection. getItemInfoByType 方法
description: GetItemInfoByType 方法會抓取對應于指定 StringCollection 索引、名稱、語言和屬性索引的值。
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- getItemInfoByType 方法 Windows Media Player
- getItemInfoByType 方法 Windows Media Player，StringCollection 類別
- StringCollection 類別 Windows Media Player，getItemInfoByType 方法
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9d270ab746618f81f7c2e4135f7a6057f207d2cc89961ebe7c8f47d9fd1abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123028"
---
# <a name="stringcollectiongetiteminfobytype-method"></a>StringCollection. getItemInfoByType 方法

**GetItemInfoByType** 方法會抓取對應于指定 **StringCollection** 索引、名稱、語言和屬性索引的值。

## <a name="syntax"></a>語法


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

**Number** (**long**) 指定要從中取得屬性之 **StringCollection** 專案的以零為基底的索引。

</dd> <dt>

*名稱* \[在\]
</dt> <dd>

包含屬性名稱的 **字串**。

</dd> <dt>

*語言* \[在\]
</dt> <dd>

包含語言的 **字串**。 如果值設定為 null 或空字串 ( "" ) 就會使用目前的地區設定字串。 否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。

</dd> <dt>

*attributeIndex* \[在\]
</dt> <dd>

**Number** (**Long**) ，其中包含要從屬性中取出之值的以零為起始的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位**、 **字串**、 **MetadataPicture** 物件或 **MetadataText** 物件，如下表所示。



| 屬性                   | 傳回值                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **數位** (不 **帶正負** 號的 long)  |
| **WM/歌詞 \_ 內容** | **MetadataText** 物件        |
| **WM/圖片**              | **MetadataPicture** 物件     |
| **WM/UserWebURL**           | **MetadataText** 物件        |
| 所有其他屬性        | String                         |



 

若為其基礎值為 **布林** 值的屬性，這個方法會傳回字串 "true" 或 "false"。

## <a name="remarks"></a>備註

這個方法支援具有多個值的屬性，以及具有複雜值的屬性。 **GetItemInfo** 方法不支援具有多個或複雜值的屬性。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MetadataPicture 物件**](metadatapicture-object.md)
</dt> <dt>

[**MetadataText 物件**](metadatatext-object.md)
</dt> <dt>

[**StringCollection. getItemInfo**](stringcollection-getiteminfo.md)
</dt> <dt>

[**StringCollection 物件**](stringcollection-object.md)
</dt> </dl>

 

 






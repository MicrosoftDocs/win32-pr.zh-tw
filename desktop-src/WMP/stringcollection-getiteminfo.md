---
title: StringCollection. getItemInfo 方法
description: GetItemInfo 方法會抓取對應于指定之 StringCollection 專案索引和名稱的字串。
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，StringCollection 類別
- StringCollection 類別 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995332"
---
# <a name="stringcollectiongetiteminfo-method"></a>StringCollection. getItemInfo 方法

**GetItemInfo** 方法會抓取對應于指定之 **StringCollection** 專案索引和名稱的字串。

## <a name="syntax"></a>語法


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
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

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串** ，表示指定之屬性的值。 針對其基礎值為 **布林** 值的屬性，它會傳回字串 "true" 或 "false"。

## <a name="remarks"></a>備註

若要使用具有複雜值的多個值和屬性來取得屬性，請使用 **getItemInfoByType** 方法。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**StringCollection. getItemInfoByType**](stringcollection-getiteminfobytype.md)
</dt> <dt>

[**StringCollection 物件**](stringcollection-object.md)
</dt> </dl>

 

 






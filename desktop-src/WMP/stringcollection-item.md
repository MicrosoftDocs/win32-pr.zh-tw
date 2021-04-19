---
title: StringCollection 專案方法
description: Item 方法會在指定的索引處捕獲字串。
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- item 方法 Windows Media Player
- item 方法 Windows Media Player，StringCollection 類別
- StringCollection 類別 Windows Media Player，item 方法
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979896"
---
# <a name="stringcollectionitem-method"></a>StringCollection 專案方法

**Item** 方法會在指定的索引處捕獲字串。

## <a name="syntax"></a>語法


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

包含索引的 (**長**) **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串**。

## <a name="remarks"></a>備註

**StringCollection** 物件是用來取得屬性可用的值集。 例如， *MediaCollection*。**getAttributeStringCollection** 方法可以用來取出 **StringCollection** 物件，代表音訊媒體類型內內容類型屬性的所有值。 然後，可以使用 item 屬性來逐一查看 [ **內容** 類型] 屬性的所有可能值。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaCollection.getAttributeStringCollection**](mediacollection-getattributestringcollection.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection 物件**](stringcollection-object.md)
</dt> </dl>

 

 






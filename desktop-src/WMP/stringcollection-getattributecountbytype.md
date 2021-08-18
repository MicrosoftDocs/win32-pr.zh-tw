---
title: StringCollection. getAttributeCountByType 方法
description: GetAttributeCountByType 方法會抓取與指定的 StringCollection 專案索引、屬性名稱和語言相關聯的屬性數目。
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- getAttributeCountByType 方法 Windows Media Player
- getAttributeCountByType 方法 Windows Media Player，StringCollection 類別
- StringCollection 類別 Windows Media Player，getAttributeCountByType 方法
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10f88a3b8e4847588ff8f7f924333c6649e59c362b3296b54ef8b83368b7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832425"
---
# <a name="stringcollectiongetattributecountbytype-method"></a>StringCollection. getAttributeCountByType 方法

**GetAttributeCountByType** 方法會抓取與指定的 **StringCollection** 專案索引、屬性名稱和語言相關聯的屬性數目。

## <a name="syntax"></a>語法


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
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

包含語言的 **字串**。 如果值設定為 null 或空字串 ( "" ) ，則會使用目前的地區設定字串。 否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位** (**long**) 。

## <a name="remarks"></a>備註

這個方法是用來判斷對應至特定 **StringCollection** 專案特定屬性名稱的屬性數目。 然後，您可以將索引編號傳遞給 **StringCollection. getItemInfoByType** 方法的第四個參數。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**StringCollection 物件**](stringcollection-object.md)
</dt> </dl>

 

 






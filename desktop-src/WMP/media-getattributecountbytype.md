---
title: GetAttributeCountByType 方法
description: GetAttributeCountByType 方法會抓取與指定的屬性名稱和語言相關聯的屬性數目。
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- getAttributeCountByType 方法 Windows Media Player
- getAttributeCountByType 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getAttributeCountByType 方法
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 222f92a57ba9fbcd9971a5536be5f31078e2e09373fb1d168a7074911b027d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123447"
---
# <a name="mediagetattributecountbytype-method"></a>GetAttributeCountByType 方法

**GetAttributeCountByType** 方法會抓取與指定的屬性名稱和語言相關聯的屬性數目。

## <a name="syntax"></a>語法


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

包含屬性名稱的 **字串**。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player[屬性參考](attribute-reference.md)。

</dd> <dt>

*語言* \[在\]
</dt> <dd>

表示語言的 **字串**。 如果值設定為 null 或 "" (空白字串) ，則會使用目前的地區設定字串。 否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位** (**long**) 包含屬性計數。

## <a name="remarks"></a>備註

這個方法是用來判斷對應至指定 **媒體** 物件之特定屬性名稱的屬性數目。 然後，您可以將索引編號傳遞給 **getItemInfoByType** 方法。 例如，當媒體專案已分類為多個內容時，這非常有用。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaObject**](media-object.md)
</dt> <dt>

[**GetItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






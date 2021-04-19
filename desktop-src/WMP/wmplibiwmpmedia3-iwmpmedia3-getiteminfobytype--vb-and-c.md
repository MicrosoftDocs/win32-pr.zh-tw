---
title: IWMPMedia3 getItemInfoByType 方法
description: GetItemInfoByType 方法會傳回對應至指定之屬性型別和索引的屬性值。
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- getItemInfoByType 方法 Windows Media Player
- getItemInfoByType 方法 Windows Media Player，IWMPMedia3 介面
- IWMPMedia3 介面 Windows Media Player，getItemInfoByType 方法
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977388"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a>IWMPMedia3：： getItemInfoByType 方法

**GetItemInfoByType** 方法會傳回對應至指定之屬性型別和索引的屬性值。

## <a name="syntax"></a>語法


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrType* \[在\]
</dt> <dd>

屬於屬性型別的 **system.string** 。

</dd> <dt>

*bstrLanguage* \[在\]
</dt> <dd>

表示語言的 **system.string** 。 如果值設定為 null 或長度為零的字串 ( "" ) ，則會使用目前的地區設定字串。 否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。

</dd> <dt>

*lIndex* \[在\]
</dt> <dd>

為屬性索引的 **system.object** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

表示屬性值的 **system.object** 。 要轉換此物件的類型取決於屬性的類型。

## <a name="remarks"></a>備註

這個方法會傳回個別數位媒體專案的中繼資料，或屬於播放清單一部分的媒體專案的中繼資料。

這個方法支援具有多個值的屬性和具有複雜值的屬性。 **GetItemInfo** 方法不支援具有多個值的屬性和具有複雜值的屬性。

**AttributeCount** 屬性會取得指定媒體專案可用的屬性名稱數目。 然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷每個可用屬性的名稱。 您可以將個別的屬性名稱傳遞給 **getItemInfoByType** 的 *name* 參數。

**GetAttributeCountByType** 方法會傳回對應至指定媒體專案特定屬性名稱的屬性數目。 然後，您可以將索引編號傳遞給 **getItemInfoByType** 的 *index* 參數。 例如，當媒體專案分類為多個內容時，這非常有用。

如果媒體專案來自呼叫 [IWMPLibrary mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)所抓取的程式庫，可用屬性的集合就會與可透過呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)所抓取的本機程式庫查詢的不同。 例如，使用 **IWMPLibrary** 抓取的本機程式庫中所提供的屬性，將會是使用 **AxWindowsMediaPlayer** 抓取之本機程式庫中可用屬性的子集。 其他來源的可用屬性集 (遠端程式庫、可攜式裝置或 Cd 是由其他來源所定義。

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMedia3 介面 (VB 和 c # )**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getAttributeName (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getAttributeCountByType (VB 和 c # )**](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 






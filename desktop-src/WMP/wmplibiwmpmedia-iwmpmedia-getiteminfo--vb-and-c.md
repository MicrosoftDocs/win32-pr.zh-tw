---
title: IWMPMedia getItemInfo 方法
description: GetItemInfo 方法會針對媒體專案傳回指定之屬性的值。
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984424"
---
# <a name="iwmpmediagetiteminfo-method"></a>IWMPMedia：： getItemInfo 方法

**GetItemInfo** 方法會針對媒體專案傳回指定之屬性的值。

## <a name="syntax"></a>語法


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrItemName* \[在\]
</dt> <dd>

**System.string** ，它是屬性的名稱。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

**System.string** ，這是指定之屬性的值。

## <a name="remarks"></a>備註

這個方法會傳回個別媒體專案的中繼資料，或屬於播放清單一部分的媒體專案的中繼資料。

**AttributeCount** 屬性會取得指定媒體專案可用的屬性名稱數目。 然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷每個可用屬性的名稱。 可以將個別的屬性名稱傳遞給 **getItemInfo**。

若要使用具有複雜值的多個值和屬性來取得屬性，請使用 **getItemInfoByType** 方法。

如果媒體專案來自呼叫 [IWMPLibrary mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)所抓取的程式庫，可用屬性的集合就會與可透過呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)所抓取的本機程式庫查詢的不同。 例如，使用 **IWMPLibrary** 抓取的本機程式庫中所提供的屬性，將會是使用 **IWMPCore** 抓取之本機程式庫中可用屬性的子集。 其他來源 (遠端程式庫、可攜式裝置或 Cd) 的可用屬性集是由其他來源所定義。

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getAttributeName (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. setItemInfo (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB 和 c # )**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 






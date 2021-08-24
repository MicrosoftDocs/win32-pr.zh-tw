---
title: IWMPStringCollection2 getItemInfobyType 方法
description: GetItemInfoByType 方法會傳回對應至指定之字串集合專案索引、名稱、語言和屬性索引的值。
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- getItemInfobyType 方法 Windows Media Player
- getItemInfobyType 方法 Windows Media Player，IWMPStringCollection2 介面
- IWMPStringCollection2 介面 Windows Media Player，getItemInfobyType 方法
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2894faedc8e2573fad5beaa7744216fbb53fbd1b090e4be2122a3194827f43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899758"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a>IWMPStringCollection2：： getItemInfobyType 方法

**GetItemInfoByType** 方法會傳回對應至指定之字串集合專案索引、名稱、語言和屬性索引的值。

## <a name="syntax"></a>語法


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a>參數

<dl> <dt>

*lCollectionIndex* \[在\]
</dt> <dd>

要從中取得屬性之字串收集項的以零為基底之索引的 **system.object。**

</dd> <dt>

*bstrType* \[在\]
</dt> <dd>

做為屬性名稱的 **system.string** 。

</dd> <dt>

*bstrLanguage* \[在\]
</dt> <dd>

表示語言的 **system.string** 。 如果值設定為 null 或零長度的字串 ( "" ) ，則會使用目前的地區設定字串。 否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。

</dd> <dt>

*lAttributeIndex* \[在\]
</dt> <dd>

以零為基底的屬性索引的 **system.object** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

表示字串收集項目的 **system.object** 。

## <a name="remarks"></a>備註

這個方法支援具有多個值的屬性和具有複雜值的屬性。 **GetItemInfo** 方法不支援具有多個值的屬性或具有複雜值的屬性。

藉由在 *bstrType* 參數中傳遞 "ChildList" 值，您就可以取出新的字串集合，其中包含父字串集合中其中一個專案的子系。 比方說，如果父集合包含 AlbumIDs 的清單，您可以使用這個方法來取得子字串集合，其中包含其中一個專輯的所有追蹤。 這種方法比呼叫 **IWMPMediaCollection2. getStringCollectionByQuery** 方法兩次更快且更有效率;一次是取得 AlbumIDs 的集合，而第二次是取得特定 AlbumID 的追蹤集合。 若要在剛剛描述的方式中使用 ChildList，必須透過 **IWMPLibraryServices** 從媒體集合取得父字串集合，而不是使用 **AxWindowsMediaPlayer. mediaCollection** 屬性。

使用 ChildList 時，請在 *bstrType* 參數中傳遞值 "ChildList"，並在 *lAttributeIndex* 參數中傳遞值0。 然後，您可以將傳回的物件轉換成 **IWMPStringCollection2** 介面，以存取子清單。

若要使用這個方法，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AlbumID 屬性**](albumid-attribute.md)
</dt> <dt>

[**IWMPLibraryServices 介面 (VB 和 c # )**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getStringCollectionByQuery (VB 和 c # )**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2 介面**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfo (VB 和 c # )**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 






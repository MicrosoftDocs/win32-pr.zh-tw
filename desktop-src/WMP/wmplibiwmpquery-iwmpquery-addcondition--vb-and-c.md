---
title: IWMPQuery addCondition 方法
description: AddCondition 方法會使用和邏輯，將條件加入至複合查詢。
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- addCondition 方法 Windows Media Player
- addCondition 方法 Windows Media Player，IWMPQuery 介面
- IWMPQuery 介面 Windows Media Player，addCondition 方法
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984772"
---
# <a name="iwmpqueryaddcondition-method"></a>IWMPQuery：： addCondition 方法

**AddCondition** 方法會使用 **和** 邏輯，將條件加入至複合查詢。

## <a name="syntax"></a>語法


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrAttribute* \[在\]
</dt> <dd>

System.string，此為要加入至查詢的屬性名稱 **。**

</dd> <dt>

*bstrOperator* \[在\]
</dt> <dd>

作為運算子的 **system.string** 。 如需支援的值，請參閱備註。

</dd> <dt>

*bstrValue* \[在\]
</dt> <dd>

表示屬性值的 **system.string** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

複合查詢中包含的條件會組織成條件群組。 條件群組內的多個條件一律會使用 **和** 邏輯串連。 條件群組一律會使用 **或** 邏輯互相串連。 若要啟動新的條件群組，請呼叫 [IWMPQuery. beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md)。

使用 **IWMPQuery** 的複合查詢不區分大小寫。

*BstrAttribute* 參數的值清單可以在 [依字母順序的屬性參考](alphabetical-attribute-reference.md)中找到。

下表列出支援的 *bstrOperator* 值。



| String              | 適用於     |
|---------------------|----------------|
| BeginsWith          | 字串        |
| 包含            | 字串        |
| 等於              | 所有類型      |
| GreaterThan         | 數位、日期 |
| GreaterThanOrEquals | 數位、日期 |
| LessThan            | 數位、日期 |
| LessThanOrEquals    | 數位、日期 |
| NotBeginsWith       | 字串        |
| NotContains         | 字串        |
| NotEquals           | 所有類型      |



 

## <a name="examples"></a>範例

下列範例會建立查詢，在其中加入兩個條件，然後使用該查詢將查詢結果以字串集合的形式解壓縮。 結果會顯示在清單方塊中。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**依字母順序排列屬性參考**](alphabetical-attribute-reference.md)
</dt> <dt>

[**IWMPMediaCollection2. createQuery (VB 和 c # )**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getPlaylistByQuery (VB 和 c # )**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getStringCollectionByQuery (VB 和 c # )**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPQuery 介面**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 






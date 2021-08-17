---
title: 'IWMPSettings. isAvailable (VB 和 C ) '
description: IsAvailable 屬性 (\_ 在 C \ ) 的 get isAvailable 方法會取得值，這個值會指出是否可以執行指定的動作。
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- IWMPSettings. isAvailable (VB 和 C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590979677e79073466f7511b3f382a4bfcebc8bf0fd8ad4cb10f6dcd957db28a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135371"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a>IWMPSettings. isAvailable (VB 和 c # ) 

**IsAvailable** 屬性 (c # 中的 **get \_ isAvailable** 方法 ) 取得值，指出是否可以執行指定的動作。


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>參數

*bstrItem*

**System.string** ，這是下列其中一個值。



| 值              | 描述                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| AutoStart          | 探索是否可以設定 [自動啟動] 屬性，以指定 Windows Media Player 自動開始播放。 |
| 餘額            | 探索是否可以使用餘額屬性來設定身歷聲平衡。                                           |
| BaseURL            | 探索是否可以設定 baseURL 屬性來指定基底 URL。                                                |
| DefaultFrame       | 探索是否可以設定 defaultFrame 屬性來指定預設框架。                                    |
| EnableErrorDialogs | 探索是否可以將 enableErrorDialogs 屬性設定為啟用或停用顯示錯誤對話方塊。        |
| GetMode            | 探索是否可以使用 getMode 方法來取得目前的迴圈或隨機模式。                          |
| InvokeURLs         | 探索是否可以設定 invokeURLs 屬性，以指定 URL 事件是否應啟動網頁瀏覽器。         |
| Mute               | 探索是否可以設定 [靜音] 屬性，以指定音訊輸出為開啟或關閉。                        |
| PlayCount          | 探索是否可以設定 playCount 屬性，以指定媒體專案將播放的次數。                 |
| 費率               | 探索是否可以設定 rate 屬性來控制播放速率。                                            |
| SetMode            | 探索 setMode 方法是否可以用來指定目前的迴圈或隨機模式。                           |
| 磁碟區             | 探索是否可以設定磁片區屬性來指定音訊卷。                                           |



 

## <a name="property-value"></a>屬性值

System.string **值，** 指出是否可以執行指定的動作。

## <a name="remarks"></a>備註

**IWMPSettings. isIdentical** 是 Visual Basic 中接受參數的屬性。 在 c # 中，它稱為 **IWMPSettings. get \_ isIdentical** 方法。

## <a name="examples"></a>範例

下列範例會使用 **isAvailable** 屬性來測試每個 **IWMPSettings** 屬性， (c # ) 中的 **get \_ isAvailable** 方法。 屬性名稱和每個測試的結果都會顯示在多行文字方塊中。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings (VB 和 c # 的 autoStart )**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[**IWMPSettings (VB 和 c # ) 的餘額**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. baseURL (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. defaultFrame (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. getMode (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. invokeURLs (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[**IWMPSettings (VB 和 c # ) 的靜音**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. playCount (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[**IWMPSettings (VB 和 c # ) 的速率**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. setMode (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings 磁片區 (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 






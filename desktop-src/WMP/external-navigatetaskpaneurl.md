---
title: NavigateTaskPaneURL 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |NavigateTaskPaneURL 方法
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- NavigateTaskPaneURL 方法 Windows Media Player
- NavigateTaskPaneURL 方法 Windows Media Player、External 類別
- External class Windows Media Player，NavigateTaskPaneURL 方法
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebcf8d799452a9966355f644f00ac5c4aecc4c066374254e8e580431b756b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649028"
---
# <a name="externalnavigatetaskpaneurl-method"></a>NavigateTaskPaneURL 方法

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**NavigateTaskPaneURL** 方法會在指定的工作窗格中開啟網頁，並將焦點變更至指定的窗格。

## <a name="syntax"></a>語法


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrKeyName* \[在\]
</dt> <dd>

**字串** ，包含線上商店的索引鍵名稱。 (必要)

</dd> <dt>

*bstrTaskPane* \[在\]
</dt> <dd>

包含網頁開啟之工作窗格名稱的 **字串**。 (必要)

</dd> <dt>

*bstrParams* \[在\]
</dt> <dd>

**字串** ，其中包含要附加至 ServiceInfo 檔的 **導覽** 元素所指定之 URL 的查詢字串參數。 (選用)

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

流覽至您的線上商店不支援的窗格，可能會導致目前的線上商店變更。

只有當從線上商店提供的網頁呼叫 **NavigateTaskPaneURL** 時，才會對 *bstrParams* 指定的值有效。

下表列出 *bstrTaskPane* 的有效值和各自的相關工作窗格。



| 值            | 工作窗格                      |
|------------------|--------------------------------|
| **ServiceTask1** | 第一個線上商店工作窗格。  |
| **ServiceTask2** | 第二個線上商店工作窗格。 |
| **ServiceTask3** | 第三個線上商店工作窗格。  |



 

載入時，您的網頁程式碼應該指定 [SelectedTaskPane](external-selectedtaskpane.md) 的值，以確保在導覽完成之後，會反白顯示正確的工作窗格按鈕。

## <a name="examples"></a>範例

下列範例程式碼示範 **NavigateTaskPaneURL** 如何建立要針對 **ServiceTask1** 顯示之網頁的 URL。

**導覽** 元素的範例：


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



呼叫 **NavigateTaskPaneURL** 方法的範例：


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



**ServiceTask1** 中顯示的網頁所產生的 URL 範例：


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型2線上商店的外部物件**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**SelectedTaskPane**](external-selectedtaskpane.md)
</dt> </dl>

 

 






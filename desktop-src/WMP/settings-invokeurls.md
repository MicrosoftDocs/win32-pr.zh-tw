---
title: 設定. invokeURLs
description: InvokeURLs 屬性會指定或抓取值，指出 URL 事件是否應該啟動網頁瀏覽器。
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- 設定. invokeURLs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977689"
---
# <a name="settingsinvokeurls"></a>設定. invokeURLs

**InvokeURLs** 屬性會指定或抓取值，指出 URL 事件是否應該啟動網頁瀏覽器。

## <a name="syntax"></a>Syntax

invokeURLs

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **布林值**。



| 值 | 描述                                  |
|-------|----------------------------------------------|
| true  | 預設值。 URL 事件應該會啟動瀏覽器。 |
| false | URL 事件不應該啟動瀏覽器。      |



 

## <a name="remarks"></a>備註

媒體檔案可以包含 Url。 將 URL 傳送至 Windows Media Player 控制項時，會先將它傳遞給 **ScriptCommand** 事件處理常式，而不論 **invokeURLs** 中的值為何。 **ScriptCommand** 結束後，Windows Media Player 會檢查 **invokeURLs** ，以判斷是否要使用 URL 啟動預設的網際網路瀏覽器。 您可以選擇性地顯示 Url，方法是在 **ScriptCommand** 中進行檢查，並視需要設定 **invokeURLs** 。

**Windows Media Player 10** 行動裝置版：此屬性只接受或傳回 false。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ScriptCommand 事件**](player-player-scriptcommand.md)
</dt> <dt>

[**Settings 物件**](settings-object.md)
</dt> </dl>

 

 






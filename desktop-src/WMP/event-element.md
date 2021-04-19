---
title: " (WMP SDK) 的事件元素"
description: 事件元素會定義在收到標記為事件的指令碼命令時，Windows Media Player 所採取的行為或動作。
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- 事件元素 Windows Media Player
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989698"
---
# <a name="event-element"></a>EVENT 元素

**事件** 元素會定義在收到標記為事件的指令碼命令時，Windows Media Player 所採取的行為或動作。

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a>屬性

需要 (**名稱**) 

事件的名稱。

**WHENDONE** (必要) 

值，這個值會定義播放參考內容之後的 Windows Media Player。

可能的值如下。



| 值  | 描述                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RESUME | 目前的專案 (由事件中斷的剪輯，) 繼續播放。 如果內容是儲存的內容，它會在停止的相同時間點繼續;如果內容是廣播，則會在目前的位置繼續進行。        |
| NEXT   | 下一個 **專案專案** 的播放方式，就像事件尚未發生，且 Windows Media Player 已到達目前剪輯的結尾。                                                                                             |
| BREAK  | 如果目前的專案是在 **重複** 迴圈內，則迴圈會結束，就像重複計數已完成一樣。 否則，Windows Media Player 會跳到播放清單的結尾，如同最後一個專案如往常般完成一樣。 |



 

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                |
|-----------------|-------------------------|
| 父元素 | **.ASX**                 |
| 子元素  | **ENTRY**、 **ENTRYREF** |



 

## <a name="remarks"></a>備註

此元素會定義在收到標記為事件的指令碼命令時，Windows Media Player 所採取的行為或動作。 事件是內嵌于資料流程的特定類型指令碼命令，會傳送至包含雙字串的 Windows Media Player。 第一個字串是 "event" 這個字，而第二個字串則是事件名稱。 第二個字串中的事件名稱必須符合中繼檔中定義的事件名稱。  (比對不區分大小寫。 ) 事件可以傳送至 Windows Media Player 接收即時串流，或是儲存在以隨選單播串流形式傳遞的 .asf、.wma 或 .wmv 檔案中。 當 Windows Media Player 收到指令碼命令時，它會處理事件，如 **事件** 元素所定義。

這個元素會定義每次 Windows Media Player 收到具有命名事件的指令碼命令時所處理的專案或 **ENTRYREF** **專案** 範圍。 **ENTRYREF** 可以是指向 ASP 頁面的 URL。 您可以使用此元素，以近乎即時的方式指定串流切換的行為，而不是使用其他內容片段或 Windows Media 中繼檔的參考，預先撰寫的資料流程變更。

當您使用 ASP 頁面產生播放清單時，必須指定 *回應* 的值。**ContentType** 屬性和 *回應*。ASP 頁面中的 **expires** 屬性，因為 Windows Media Player 的延遲問題。 *回應*。**ContentType** 必須是有效的 Windows Media 中繼檔副檔名。 有效類型包括 .asf、.asx、.wma、. 地板蠟、.wmv 和. 300k.wvx。

如需在 ASP 中使用 **回應** 物件的詳細資訊，請參閱 Platform SDK。

這個元素可以出現在 **ASX** 元素內的任何位置。 如果 **asx** 專案中有多個 **事件** 元素的 **名稱** 屬性具有相同的值，Windows Media Player 會使用 **ASX** 元素內的第一個相符專案，並忽略所有其他專案。 當 **事件** 元素有相異的 **名稱** 屬性時，在 **ASX** 元素內的順序並不重要。

Windows Media Player 會捨棄它在處理另一個事件時所收到的事件。 不支援事件的嵌套。 當 Windows Media Player 處於預覽模式時，事件內容不受 **PREVIEWDURATION** 元素的限制;即使作用中 **專案專案** 的預覽持續時間在事件結束之前過期，也可以播放事件內容的完整長度。

## <a name="examples"></a>範例

在此範例中，當 Windows Media Player 在其呈現的串流媒體中收到指令碼命令事件和命令字串 "Adlink" 時，它會在播放清單中搜尋 **事件名稱** "Adlink"。 Windows Media Player 從正在轉譯的資料流程切換，並播放 **事件** 中所參考的內容： " https://example.microsoft.com/adlink.htm "。

**專案** 屬性 **CLIENTSKIP** 設定為 [否]，以防止略過 **事件** 剪輯。 必須加以播放。

腳本 `WHENDONE="RESUME"` 會指示 Windows Media Player 在 Adlink 完成時，繼續播放先前切換的媒體。


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> <dt>

[**Windows Media Player 物件模型**](windows-media-player-object-model.md)
</dt> </dl>

 

 






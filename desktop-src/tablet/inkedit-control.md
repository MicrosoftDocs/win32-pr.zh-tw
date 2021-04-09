---
description: InkEdit 控制項提供簡單的方式來捕捉、辨識和顯示筆墨。
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: InkEdit 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d5441506ee791eefddba05b9b1f3ddb8a8ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850023"
---
# <a name="inkedit-control"></a>InkEdit 控制項

[InkEdit](inkedit-control-reference.md)控制項提供簡單的方式來捕捉、辨識和顯示筆墨。

這種 [InkEdit](inkedit-control-reference.md) 控制項的執行是以 [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) 控制項為基礎。 Managed ( .NET Framework) 的 [InkEdit](/previous-versions/ms835842(v=msdn.10)) 執行是以 [**RichTextBox**](/previous-versions/windows/) 控制項為基礎。

[InkEdit](inkedit-control-reference.md)控制項的主要目的是要收集筆跡、加以辨識，並以文字形式顯示。 此外，它支援將筆墨顯示為具有文字格式設定功能的内嵌物件，例如粗體和底線。

## <a name="gestures-and-correction"></a>手勢和修正

[InkEdit](inkedit-control-reference.md) 支援下列手勢。



| 手勢                                                                    | 手勢名稱              | 動作               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![向左手勢](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | 向左<br/>      | Enter<br/>     |
| ![向左移長的手勢](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | 向左至左-long<br/> | Enter<br/>     |
| ![右上手勢](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | 右上方<br/>       | 索引標籤<br/>       |
| ![最右側的手勢。](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | 右上-long<br/>  | 索引標籤<br/>       |
| ![右手勢](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | Right<br/>          | Space<br/>     |
| ![左方手勢](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | Left<br/>           | 退格鍵<br/> |



 

您可以處理的手勢事件包含手勢、筆劃和游標資訊，您可以用來傳送文字以 [InkEdit](inkedit-control-reference.md) 或將資料放在剪貼簿上。

[InkEdit](inkedit-control-reference.md) 也提供更正使用者介面，可讓使用者從替代項中進行流覽和選取、使用螢幕小鍵盤，以及字元/字母/封鎖辨識器。

## <a name="other-details"></a>其他詳細資料

[InkEdit](inkedit-control-reference.md) 的設計可在單一行的表單案例中，以及多行文字輸入和編輯的情況下運作。 InkEdit 的主要用途是從使用者以手寫形式取得文字輸入。 根據預設，會辨識筆跡輸入，並在其位置插入文字。 InkEdit 的預設使用者介面類別似于 [**RichTextBox**](/previous-versions/windows/) 控制項，但使用者正在配置筆墨時除外。 您可以顯示原始筆跡而非文字;不過，筆墨會調整為 InkEdit 控制項目前的輸入字型大小，並以內嵌方式顯示在其他文字中。

> [!Note]  
> 基於安全性考慮，您必須使用標準程式來開啟或關閉檔案、串流輸入/輸出，以及設定 [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) 或 [**文本**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) 屬性。

 

[InkEdit](inkedit-control-reference.md)控制項預設會設定為將筆墨辨識為文字。 若要讓使用者將筆墨新增為筆墨，請將 [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) 屬性設定為 **InsertAsInk**。

如需 [InkEdit](inkedit-control-reference.md) 控制項的詳細參考資訊，請參閱 InkEdit。

> [!Note]  
> 如果您使用 Win32 [InkEdit](inkedit-control-reference.md) 控制項，並將它放在群組方塊內，請確定方塊具有透明樣式;否則，InkEdit 就無法收集筆跡。

 

> [!Note]  
> 若要確保筆墨正確顯示，請在收到 [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1)或 [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1)事件時呼叫 [InkEdit](inkedit-control-reference.md) [**控制項重新**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh)整理方法。

 

下列各節詳細說明 [InkEdit](inkedit-control-reference.md) 控制項的使用：

-   [具現化 InkEdit](instantiating-inkedit.md)
-   [單字與字元識別的比較](word-vs--character-recognition.md)
-   [將筆墨顯示為筆墨](displaying-ink-as-ink.md)
-   [在舊版 Windows 上使用 InkEdit](using-inkedit-on-earlier-versions-of-windows.md)
-   [使用應用程式字典搭配 InkEdit](using-an-application-dictionary-with-inkedit.md)

 


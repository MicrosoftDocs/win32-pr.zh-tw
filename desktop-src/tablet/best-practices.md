---
description: 使用 [畫筆輸入面板] 物件時的最佳作法總覽。
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: " (Tablet PC) 的最佳作法"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195324"
---
# <a name="best-practices-tablet-pc"></a> (Tablet PC) 的最佳作法

使用 [**PenInputPanel**](peninputpanel-class.md) 物件時，請記住一些指導方針。

-   [偏好 InkEdit 控制項](#prefer-inkedit-control)
-   [停用 InkEdit 控制項的筆墨模式](#disable-ink-mode-on-inkedit-controls)
-   [使用無視窗控制項](#using-windowless-controls)
-   [相關主題](#related-topics)

## <a name="prefer-inkedit-control"></a>偏好 InkEdit 控制項

[InkEdit](inkedit-control-reference.md) 是要附加 [**PenInputPanel**](peninputpanel-class.md) 物件的慣用控制項。 InkEdit 控制項提供 [文字服務架構 (TSF) ](text-services-framework.md)的支援。

## <a name="disable-ink-mode-on-inkedit-controls"></a>停用 InkEdit 控制項的筆墨模式

附加至 [InkEdit](inkedit-control-reference.md) 控制項時，請將 InkEdit 控制項的 [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) 屬性設定為 [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) 值。 如果 [ **InkMode** ] 屬性未設定為 [ **InkMode** ] 值，則 InkEdit 控制項會將第一點點轉譯為筆劃、將其傳遞至辨識器，然後將文字插入 InkEdit 控制項中。 因為您已經附加 [**PenInputPanel**](peninputpanel-class.md) 物件來接受筆跡輸入，所以不需要也為筆墨輸入啟用 InkEdit 控制項。

## <a name="using-windowless-controls"></a>使用無視窗控制項

將 [**PenInputPanel**](peninputpanel-class.md) 物件附加至包含多個無視窗控制項的父視窗時， **PenInputPanel** 物件不知道如何在將焦點移到無視窗的子系時追蹤插入號。 當輸入暫止時，當焦點從一個無視窗控制項移至另一個控制項時，手寫輸入可以傳送至錯誤的子系。

若要在無視窗環境中使用 [**PenInputPanel**](peninputpanel-class.md) 物件，您可以使用下列技術：

1.  將 [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) 控制項具現化，並將它放在無視窗控制項上。
2.  將 [**PenInputPanel**](peninputpanel-class.md) 物件附加至新的文字方塊控制項。
3.  讓文字方塊控制項收集 [**PenInputPanel**](peninputpanel-class.md) 物件中的已辨識文字。
4.  當焦點變更離開文字方塊控制項時，呼叫 [**PenInputPanel**](peninputpanel-class.md)物件的 [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput)方法。
5.  將已辨識的文字從文字方塊控制項複製到無視窗子系。
6.  將 [**PenInputPanel**](peninputpanel-class.md) 物件的 [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (僅限 managed 程式碼) 屬性或 [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) 屬性設定為 null，以卸離該物件。
7.  終結文字方塊控制項。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**PenInputPanel 類別**](peninputpanel-class.md)
</dt> <dt>

[PenInputPanel](/previous-versions/ms583923(v=vs.100))
</dt> <dt>

[Text Services Framework (TSF)](../tsf/text-services-framework.md)
</dt> </dl>

 

 

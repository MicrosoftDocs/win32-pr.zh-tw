---
title: 主題元素
description: 主題元素
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Windows Media Player 的外觀，主題元素
- 外觀，主題元素
- 主題元素
- 外觀的參考，主題元素
- 元素，主題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c15091ffa93e3ae64a06979580931c27bdf4c1cd2e26c7acc206d76de8b0fc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507388"
---
# <a name="theme-element"></a>主題元素

**主題** 元素是面板的父層級元素，並包含一或多個 **VIEW** 元素，這些元素接著會包含面板中的所有其他專案。 在腳本程式碼中，**主題** 專案是透過 **主題** 全域屬性來存取，而不是透過 [**主題**] 專案不支援的 **識別碼** 屬性所指定的名稱來存取。

**主題** 元素支援下列屬性。



| 屬性                                | 描述                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [作者](theme-author.md)               | 指定或抓取面板的作者名稱。                                                                      |
| [authorVersion](theme-authorversion.md) | 指定或抓取作者指派的面板版本號碼。                                                |
| [版權](theme-copyright.md)         | 指定或抓取面板的著作權字串。                                                                       |
| [currentViewID](theme-currentviewid.md) | 指定或抓取目前顯示的 **視圖**。                                                                        |
| [title](theme-title.md)                 | 指定或抓取面板的標題。                                                                                   |
| [version](theme-version.md)             | 指定或抓取用來撰寫面板的 Windows Media Player 版本號碼。 只能在設計階段設定。 |



 

**主題** 元素支援下列方法。



| 方法                                         | 描述                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [closeView](theme-closeview.md)               | 關閉開啟的 **視圖**。                                                                                        |
| [loadPreference](theme-loadpreference.md)     | 從登錄載入喜好設定。                                                                           |
| [logString](theme-logstring.md)               | 如果啟用記錄功能，則將使用者定義的字串記錄至錯誤檔。                                            |
| [openDialog](theme-opendialog.md)             | 開啟 [檔案] 對話方塊。                                                                                        |
| [openView](theme-openview.md)                 | 在新視窗中開啟一個 **VIEW** 。                                                                               |
| [openViewRelative](theme-openviewrelative.md) | 在相對於面板左上角的指定初始位置，在新視窗中開啟一個 **VIEW** 。 |
| [playSound](theme-playsound.md)               | 播放指定的音效檔。                                                                                 |
| [savePreference](theme-savepreference.md)     | 將喜好設定儲存在登錄中。                                                                             |
| [showErrorDialog](theme-showerrordialog.md)   | 顯示 [標準錯誤] 對話方塊。                                                                         |



 

**主題** 元素不支援事件處理常式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 





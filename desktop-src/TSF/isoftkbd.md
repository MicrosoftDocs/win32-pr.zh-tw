---
title: 'ISoftKbd 介面 (Softkbdc .h) '
description: 應用程式和文字服務會使用 ISoftKbd 介面來執行軟鍵盤。
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- ISoftKbd 介面文字服務架構
- ISoftKbd 介面文字服務架構，說明
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965690"
---
# <a name="isoftkbd-interface"></a>ISoftKbd 介面

應用程式和文字服務會使用 **ISoftKbd** 介面來執行軟鍵盤。

## <a name="members"></a>成員

**ISoftKbd** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ISoftKbd** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISoftKbd** 介面具有這些方法。



| 方法                                                                                        | 描述                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**AdviseSoftKeyboardEventSink**](isoftkbd-advisesoftkeyboardeventsink.md)                   | 安裝軟鍵盤事件接收器，以從螢幕小鍵盤處理 OnKeySelection 通知。<br/> |
| [**CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md) | 從指定的資源建立軟鍵盤版面配置。<br/>                                        |
| [**CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | 從指定的 XML 檔案建立軟鍵盤版面配置。<br/>                                        |
| [**CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)                         | 建立軟鍵盤視窗。<br/>                                                                    |
| [**DestroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)                       | 終結軟鍵盤視窗。<br/>                                                                   |
| [**EnumSoftKeyboard**](isoftkbd-enumsoftkeyboard.md)                                         | 列舉支援指定語言的可能軟鍵盤。<br/>                        |
| [**GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)                               | 抓取與所提供色彩類型對應的軟鍵盤色彩。<br/>                        |
| [**GetSoftKeyboardPosSize**](isoftkbd-getsoftkeyboardpossize.md)                             | 抓取軟鍵盤的開始位置和大小。<br/>                                       |
| [**GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)                           | 抓取軟鍵盤所使用的文字字型。<br/>                                                   |
| [**GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)                           | 抓取軟鍵盤的類型模式。<br/>                                                       |
| [**初始化**](isoftkbd-initialize.md)                                                     | 初始化軟鍵盤的所有必要欄位，並產生標準的軟鍵盤配置。<br/> |
| [**SelectSoftKeyboard**](isoftkbd-selectsoftkeyboard.md)                                     | 選取指定的軟鍵盤。<br/>                                                               |
| [**SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)                                 | 從軟鍵盤的版面配置設定標籤文字。<br/>                                           |
| [**SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)           | 設定用來描述軟鍵盤的標籤和文字的組合。<br/>                             |
| [**SetSoftKeyboardColors**](isoftkbd-setsoftkeyboardcolors.md)                               | 設定對應于所提供色彩類型的軟鍵盤色彩。<br/>                             |
| [**SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)                             | 設定軟鍵盤的開始位置和大小。<br/>                                            |
| [**SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)                           | 設定軟鍵盤所使用的文字字型。<br/>                                                        |
| [**SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)                           | 設定軟鍵盤的類型模式。<br/>                                                            |
| [**ShowKeysForKeyScanMode**](isoftkbd-showkeysforkeyscanmode.md)                             | 顯示軟鍵盤的金鑰掃描模式所使用的金鑰。<br/>                                  |
| [**ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)                                         | 顯示軟鍵盤。<br/>                                                                          |
| [**UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)               | 移除軟鍵盤事件接收器。<br/>                                                                |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Softkbdc。h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



 


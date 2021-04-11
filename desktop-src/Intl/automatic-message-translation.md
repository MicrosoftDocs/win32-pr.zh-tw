---
description: 使用 Unicode 和字元集 API 函數的應用程式通常會使用相同的視窗類別。 作業系統會以透明的方式轉譯不同類別的視窗之間的訊息。
ms.assetid: 68e9839b-39f8-411a-8ae4-4a627c667cae
title: 自動訊息轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b02a5c5a4951189333608aa448f09ba9c6866d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690260"
---
# <a name="automatic-message-translation"></a>自動訊息轉譯

使用 Unicode 和字元集 API 函數的應用程式通常會使用相同的視窗類別。 作業系統會以透明的方式轉譯不同類別的視窗之間的訊息。

執行的視窗函式會以 Unicode 或 Windows 字碼頁格式接收訊息。 視窗函數可以傳送訊息或呼叫任一個類型的函式。

下列訊息有文字引數，且受限於自動文字翻譯。 如需自動轉譯的詳細資訊，請參閱子類別化 [和自動訊息轉譯](subclassing-and-automatic-message-translation.md)。

<dl>

[CB \_ ADDSTRING](../controls/cb-addstring.md)  
[CB \_ 目錄](../controls/cb-dir.md)  
[CB \_ FINDSTRING](../controls/cb-findstring.md)  
[CB \_ GETLBTEXT](../controls/cb-getlbtext.md)  
[CB \_ INSERTSTRING](../controls/cb-insertstring.md)  
[CB \_ SELECTSTRING](../controls/cb-selectstring.md)  
[EM \_ GETLINE](../controls/em-getline.md)  
[EM \_ REPLACESEL](../controls/em-replacesel.md)  
[EM \_ SETPASSWORDCHAR](../controls/em-setpasswordchar.md)  
[LB \_ ADDFILE](../controls/lb-addfile.md)  
[LB \_ ADDSTRING](../controls/lb-addstring.md)  
[LB \_ 目錄](../controls/lb-dir.md)  
[LB \_ FINDSTRING](../controls/lb-findstring.md)  
[LB \_ GETTEXT](../controls/lb-gettext.md)  
[LB \_ INSERTSTRING](../controls/lb-insertstring.md)  
[LB \_ SELECTSTRING](../controls/lb-selectstring.md)  
[WM \_ ASKCBFORMATNAME](../dataxchg/wm-askcbformatname.md)  
[WM \_ 字元](../inputdev/wm-char.md)  
[WM \_ CHARTOITEM](../controls/wm-chartoitem.md)  
[WM \_ 建立](../winmsg/wm-create.md)  
[WM \_ DEADCHAR](../inputdev/wm-deadchar.md)  
[WM \_ DEVMODECHANGE](../gdi/wm-devmodechange.md)  
[WM \_ GETTEXT](../winmsg/wm-gettext.md)  
[WM \_ MDICREATE](../winmsg/wm-mdicreate.md)  
[WM \_ MENUCHAR](../menurc/wm-menuchar.md)  
[WM \_ NCCREATE](../winmsg/wm-nccreate.md)  
[WM \_ SETTEXT](../winmsg/wm-settext.md)  
[WM \_ SYSCHAR](../menurc/wm-syschar.md)  
[WM \_ SYSDEADCHAR](../inputdev/wm-sysdeadchar.md)  
[WM \_ WININICHANGE](../winmsg/wm-wininichange.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows API 中的 Unicode](unicode-in-the-windows-api.md)
</dt> </dl>

 

 

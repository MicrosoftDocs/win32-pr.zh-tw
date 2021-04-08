---
title: 無視窗的 Rich Edit 控制項
description: 本章節包含與無視窗 rich edit 控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021052"
---
# <a name="windowless-rich-edit-controls"></a>無視窗的 Rich Edit 控制項

本章節包含與無視窗 rich edit 控制項搭配使用之程式設計項目的相關資訊。 元件物件模型 (COM) 會定義一組介面，以支援無視窗的物件。 無視窗物件可以輸入就地作用中狀態，而不需要自己的視窗，而是使用其容器的視窗。 因此，無視窗物件會使用較少的系統資源，並透過更快速的啟用和停用提供更佳的效能。 此外，無視窗的物件可以是非矩形且透明的。

### <a name="overviews"></a>概觀



| 主題                                                                          | 目錄                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於無視窗的 Rich Edit 控制項](about-windowless-rich-edit-controls.md) | 無視窗的 rich edit 控制項（也稱為文字服務物件）是一種物件，可提供 [豐富編輯控制項](rich-edit-controls.md) 的功能，而不需提供視窗。<br/> |



 

### <a name="functions"></a>函式



| 主題                                            | 目錄                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices)函式會建立文字服務物件的實例。 文字服務物件支援各種不同的介面，包括 [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) 和 Text 物件模型 (TOM) 。<br/> |



 

### <a name="interfaces"></a>介面



| 主題                                  | 目錄                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)介面是由文字服務物件用來取得文字主機服務。<br/> |
| [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) | 擴充 TOM 以提供無視窗操作的額外功能。<br/>                                     |



 

 

 






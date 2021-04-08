---
title: Windows 控制項
description: 控制項是應用程式用來與另一個視窗結合以啟用使用者互動的子視窗。
ms.assetid: 0a6eb481-d94e-40c5-afec-46354520f08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bf14f3c93f6f38ba787cba463977a4dca9eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021053"
---
# <a name="windows-controls"></a>Windows 控制項

## <a name="purpose"></a>目的

控制項是應用程式用來與另一個視窗結合以啟用使用者互動的子視窗。 控制項最常用於對話方塊內，但也可以在其他視窗中使用。 對話方塊內的控制項可讓使用者輸入文字、選擇選項，以及起始動作。 其他視窗中的控制項提供各種不同的服務，例如讓使用者選擇命令、查看狀態，以及查看和編輯文字。 本檔說明 Windows 所提供的控制項，以及用來建立和操作這些控制項的程式設計項目。

如需所有 Windows 控制項的清單，包括每個控制項的完整總覽和參考資訊的連結，請參閱 [控制項程式庫](individual-control-info.md)。

## <a name="developer-audience"></a>開發人員對象

控制項是設計來供 C/c + + 開發人員和 UI 設計人員使用。 一般情況下，開發人員需要對 UI 程式設計概念、Windows API 程式設計和 Unicode 進行中等程度的瞭解。

## <a name="run-time-requirements"></a>執行階段需求求

控制項的支援是由 User32.dll 和 Comctl32.dll 所提供。 如需詳細資訊，請參閱 [通用控制項版本](common-control-versions.md)。

## <a name="in-this-section"></a>本節內容



| 主題                                                                             | 描述                                                                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於通用控制項](common-controls-intro.md)<br/>                     | 提供 Comctl32.dll 所支援的所有控制項通用的一般資訊。<br/>                                      |
| [控制訊息](control-messages.md)<br/>                               | 說明如何使用 Windows 訊息與控制項通訊。<br/>                                                                 |
| [自訂控制項](user-controls-intro.md)<br/>                             | 描述建立自訂控制項的各種方式。 <br/>                                                                                 |
| [子類別化控制項](subclassing-overview.md)<br/>                       | 描述透過變更或加入新的功能來自訂控制項的方式。 <br/>                                                 |
| [自訂繪圖](custom-draw.md)<br/>                                         | 描述由某些控制項提供的服務，應用程式可以使用這些控制項來自訂控制面板的各種層面。 <br/> |
| [安全性考慮： Microsoft Windows 控制項](sec-comctls.md)<br/> | 提供與 Windows 控制項相關之安全性考慮的資訊。 <br/>                                                 |
| [控制項程式庫](individual-control-info.md)<br/>                         | 提供有關 User32.dll 和 Comctl32.dll 所支援之每個控制項的總覽和參考資訊。<br/>                            |
| [一般控制項參考](common-control-reference.md)<br/>              | 提供適用于多個控制項之程式設計專案的參考資訊，而不只是特定的控制項。<br/>           |
| [控制 Spy 2.0 版](control-spy.md)<br/>                                    | 描述 Control Spy，這是可協助開發人員瞭解通用控制項的工具。 <br/>                                                     |
| [視覺化樣式](themes-overview.md)<br/>                                   | 說明如何根據使用者選擇的視覺化樣式來變更控制項的外觀。 <br/>                               |
| [主題檔案格式](themesfileformat-overview.md)<br/>                     | 討論主題 ( 的格式) Windows 7 和 Windows Vista 中使用的檔。<br/>                                                    |



 

 

 






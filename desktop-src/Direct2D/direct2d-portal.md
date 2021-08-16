---
title: Direct2D
description: Direct2D
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d685c62819fe97e7ca52a566a0e2d442f5e4be14d6b7ae0a252b2778c0bae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825419"
---
# <a name="direct2d"></a>Direct2D

## <a name="purpose"></a>目的

Direct2D 是一種硬體加速的即時模式 2D 圖形 API，能夠以高效能和高品質來呈現 2D 幾何、點陣圖和文字。 Direct2D API 的設計目的是要與 GDI、GDI+ 和 Direct3D 妥善地交互操作。

## <a name="developer-audience"></a>開發人員對象

Direct2D 主要是設計來供下列開發人員類別使用：

-   大型企業規模原生應用程式的開發人員。
-   建立可供下游開發人員取用的控制項工具組和程式庫的開發人員。
-   需要伺服器端呈現2D 圖形的開發人員。
-   使用 Direct3D 圖形並需要簡單、高效能的2D 和文字轉譯（用於功能表、使用者介面 (UI) 專案），以及顯示 (HUDs) 的開發人員。

## <a name="run-time-requirements"></a>執行階段需求求

-   Windows 7 或 Windows vista （含 Service Pack 2） (SP2) 和 Windows vista 和更新版本的平臺更新。
-   Windowsserver 2008 R2 或 Windows server 2008 Service Pack 2 (SP2) 以及 Windows Server 2008 和更新版本的平臺更新。

> [!Note]
>
> 適用于 Windows Server 2008 Windows Vista 和平臺更新的平臺更新是一組執行時間程式庫，可讓開發人員將應用程式的目標設為 Windows 7、Windows Vista、Windows server 2008 R2 和 Windows server 2008。 所有 Windows Vista 和 Windows Server 2008 客戶都可以透過 Windows Update 取得這些更新。 需要適用于 Windows Server 2008 Windows Vista 或平臺更新的協力廠商應用程式，可以讓 Windows Update 偵測是否已安裝必要的更新;如果不是，Windows Update 會在背景中下載並安裝它。 如需這兩項更新的詳細資訊，請參閱[Windows Vista 的平臺更新](https://support.microsoft.com/kb/971644)。

 

## <a name="in-this-section"></a>本節內容



| 主題                                                                                          | 描述                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Direct2D 的新功能](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | 以下是一些 Direct2D 新增專案。 <br/>                                                                                                                   |
| [關於 Direct2D](direct2d-overview.md)<br/>                                             | 介紹 Direct2D，這是一個 API，可讓 Win32 開發人員能夠執行具有優異效能和視覺品質的2D 圖形轉譯工作。 <br/> |
| [Windows 8 的 Direct2D 快速入門](direct2d-quickstart-with-device-context.md)<br/>    | 摘要說明使用 Direct2D 進行繪製所需的步驟，並提供範例程式碼。<br/>                                                                                     |
| [使用 Direct2D 開始使用](getting-started-with-direct2d-nav.md)<br/>              | 說明如何開始建立 Direct2D 應用程式，並提供範例程式碼。<br/>                                                                             |
| [程式設計指南](programming-guide.md)<br/>                                          | 本節包含描述如何使用 Direct2D API 的概念程式設計主題。 <br/>                                                                    |
| [Direct2D 參考](reference.md)<br/>                                                      | 詳細說明 Direct2D API。<br/>                                                                                                                              |
| [工具和公用程式](tools-and-utilities.md)<br/>                                      | 為 Direct2D 提供的工具和公用程式。<br/>                                                                                                                         |
| [範例](d2d-samples.md)<br/>                                                          | 示範 Direct2D API 的範例應用程式。<br/>                                                                                                             |
| [Direct2D 詞彙](direct2d-glossary.md)<br/>                                          | 描述 Direct2D 檔一般使用的詞彙。 <br/>                                                                                                      |



 

## <a name="additional-resources"></a>其他資源

-   [**DirectX 圖形與遊戲**](/windows/desktop/directx)
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)

 


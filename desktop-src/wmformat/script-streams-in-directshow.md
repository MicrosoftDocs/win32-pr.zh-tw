---
title: DirectShow 中的腳本資料流程
description: DirectShow 中的腳本資料流程
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows媒體格式 SDK，DirectShow
- Windows媒體格式 SDK，腳本資料流程
- Advanced Systems Format (ASF) ，DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、腳本資料流程
- ASF (Advanced 系統格式) 、腳本資料流程
- DirectShow，腳本資料流程
- 腳本資料流程，DirectShow
- 資料流程，DirectShow 中的腳本資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30e832928b84ab0e1e755dcfdb8c79893c5d942e15e4beb9925f852251614bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929617"
---
# <a name="script-streams-in-directshow"></a>DirectShow 中的腳本資料流程

當「WM ASF 讀取器」篩選器指定包含 WMMEDIATYPE 腳本類型資料流程的檔案時 \_ ，它會為它建立輸出圖釘，以便連接到 DirectShow 內部指令碼命令轉譯器篩選器。 當您呼叫 **IGraphBuilder：： RenderFile** 時，該篩選會自動加入至圖形並連接。 當內部指令碼命令轉譯器收到包含指令碼命令的範例時，它會引發 **lParam** 包含腳本的 **EC \_ OLE \_ 事件**。 應用程式完全負責處理這個事件。 如需有關 **EC \_ OLE \_ 事件** 的詳細資訊，請參閱 DirectShow SDK 檔。

 

 





---
title: 在 DirectShow 中編寫串流的腳本
description: 在 DirectShow 中編寫串流的腳本
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows Media Format SDK、DirectShow
- Windows Media Format SDK，腳本資料流程
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、腳本資料流程
- ASF (Advanced 系統格式) 、腳本資料流程
- DirectShow，腳本資料流程
- 腳本串流，DirectShow
- 串流，在 DirectShow 中編寫串流腳本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311157"
---
# <a name="script-streams-in-directshow"></a>在 DirectShow 中編寫串流的腳本

當「WM ASF 讀取器」篩選器指定包含 WMMEDIATYPE 腳本類型資料流程的檔案時 \_ ，它會為它建立輸出圖釘，以連接至 DirectShow 內部指令碼命令轉譯器篩選器。 當您呼叫 **IGraphBuilder：： RenderFile** 時，該篩選會自動加入至圖形並連接。 當內部指令碼命令轉譯器收到包含指令碼命令的範例時，它會引發 **lParam** 包含腳本的 **EC \_ OLE \_ 事件**。 應用程式完全負責處理這個事件。 如需有關 **EC \_ OLE \_ 事件** 的詳細資訊，請參閱 DirectShow SDK 檔。

 

 





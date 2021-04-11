---
description: DirectShow 中的 ASF 腳本資料流程
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: DirectShow 中的 ASF 腳本資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935925"
---
# <a name="asf-script-streams-in-directshow"></a>DirectShow 中的 ASF 腳本資料流程

當您為 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器指定包含 WMMEDIATYPE 腳本類型資料流程的檔案時 \_ ，它會為它建立輸出圖釘，以連接到 [內部指令碼命令](internal-script-command-renderer-filter.md) 轉譯器篩選器。 當您呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)時，該篩選會自動加入至圖形並連接。 當內部指令碼命令轉譯器收到包含指令碼命令的範例時，它會引發 *lParam* 包含腳本的 [**EC \_ OLE \_ 事件**](ec-ole-event.md)事件。 應用程式完全負責處理這個事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中讀取 ASF 檔案](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




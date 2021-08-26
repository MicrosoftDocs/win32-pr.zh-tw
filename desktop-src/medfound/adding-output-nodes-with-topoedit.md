---
description: 使用 TopoEdit 新增輸出節點
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: 使用 TopoEdit 新增輸出節點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e975e332a464218f8629363f34a2d3fbef0e5a49
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481974"
---
# <a name="adding-output-nodes-with-topoedit"></a>使用 TopoEdit 新增輸出節點

在拓撲中，輸出節點代表從轉換節點接收媒體資料並呈現播放的媒體接收。 輸出節點的類型取決於來源節點的媒體類型。

下表顯示將輸出節點加入拓撲的功能表/工具列命令。




| 來源媒體類型 | 功能表/工具列命令 | Description | 
|-------------------|----------------------|-------------|
| 音訊資料流 | 在 [ <strong>拓撲</strong> ] 功能表上，按一下 [ <strong>新增 SAR</strong>]。 | 建立串流音訊轉譯器的輸出節點， (SAR) 透過音訊裝置（例如音效卡）播放音訊串流。 | 
| 影片串流 | 在 [ <strong>拓撲</strong> ] 功能表上，按一下 [ <strong>新增 EVR</strong>]。 | 建立增強型影片轉譯器的輸出節點 (EVR) ，以顯示影片串流的畫面格。 | 
| 自訂媒體接收 | <ol><li>在 [ <strong>拓撲</strong> ] 功能表上，按一下 [ <strong>新增自訂接收</strong>]。<br /> [ <strong>輸入自訂 GUID</strong> ] 對話方塊隨即開啟。<br /></li><li><p>在 [ <strong>GUID：</strong> ] 欄位中，輸入您要新增至拓撲的自訂接收的 GUID。<br /></p><blockquote>[!Note]<br />TopoEdit 會預期格式為 "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" 的 GUID。 否則，它無法新增節點，並會顯示「不正確 GUID」錯誤訊息。</blockquote><p><br /></p></li><li>按一下 [確定]。<br /></li></ol> | 為自訂媒體來源的資料流程接收建立輸出節點。<br /> 自訂接收必須支援 <strong>CoCreateInstance</strong> ，才能以 CLSID 指定接收。<br /> | 




 

TopoEdit 會建立指定的輸出節點。 [ **拓撲] 窗格** 會將輸出節點顯示為顯示資料流程接收名稱的綠色方塊。

如需使用媒體基礎 Api 以程式設計方式加入輸出節點的詳細資訊，請參閱 [建立輸出節點](creating-output-nodes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 TopoEdit 建立拓撲](building-topologies-by-using-topoedit.md)
</dt> <dt>

[串流音訊轉譯器](streaming-audio-renderer.md)
</dt> <dt>

[增強的影片轉譯器](enhanced-video-renderer.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 





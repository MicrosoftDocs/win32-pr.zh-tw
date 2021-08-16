---
description: 使用 TopoEdit 建立播放拓撲
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: 使用 TopoEdit 建立播放拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a71ae353c11108fe7c844d8ddd6441e652e007646b91f44c6fe2b480a22a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035426"
---
# <a name="building-a-playback-topology-with-topoedit"></a>使用 TopoEdit 建立播放拓撲

TopoEdit 可以自動新增並連接來源、轉換和輸出節點，以建立本機媒體檔案的播放拓撲。 TopoEdit 不會自動解析拓撲。 若要播放拓撲，請加以解決，然後使用傳輸控制項。

## <a name="to-build-and-play-a-topology-for-a-media-file"></a>若要建立並播放媒體檔案的拓撲

1.  **在 [檔案**] 功能表上 **，按一下 [** 轉譯檔案]。

    這會開啟 [ **選取媒體來源** ] 對話方塊。

2.  流覽至媒體檔案所在的資料夾。
3.  在 [ **檔案名：** ] 欄位中，輸入檔案的名稱。
4.  按一下 [開啟]。

    [ **拓撲] 窗格** 會顯示已連線的拓撲。 就內部而言，TopoEdit 會執行下列工作：

    -   列舉媒體檔案中的資料流程，並建立來源節點。
    -   視來源節點的媒體類型而定，會加入轉換節點，例如「解碼器」。
    -   將音訊串流的串流音訊轉譯器 (特別行政區) 接收，以及增強的影片轉譯器 (EVR 影片串流的) 接收器。
    -   連接節點輸入和節點輸出。

5.  在 [ **拓撲** ] 功能表上，按一下 [ **解析拓撲**]。
6.  按一下工具列上的 [ **播放** ] 按鈕來播放拓撲。 下圖顯示 [ **播放** ] 按鈕 :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[TopoEdit 中的播放控制項](playback-controls-in-topoedit.md)
</dt> <dt>

[使用 TopoEdit 解析拓撲](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




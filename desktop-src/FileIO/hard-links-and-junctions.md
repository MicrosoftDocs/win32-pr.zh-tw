---
description: 描述永久連結和接合。
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: 永久連結和接合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376ed8b3bbe163d2bad4b8c51715537e194633f02ec200ceb5df02df7d582ae3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107447"
---
# <a name="hard-links-and-junctions"></a>永久連結和接合

NTFS 檔案系統支援三種類型的檔案連結：永久連結、接合和符號連結。 本主題概述永久連結和連接。 如需符號連結的詳細資訊，請參閱 [建立符號連結](creating-symbolic-links.md)。

## <a name="hard-links"></a>永久連結

*硬式連結* 是檔案的檔案系統表示，其中有一個以上的路徑參考相同磁片區中的單一檔案。 若要建立硬式連結，請使用 [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) 函數。 對該檔案所做的任何變更都會立即顯示給應用程式，透過參考該檔案的永久連結來存取該檔案。 不過，目錄專案大小和屬性資訊只會針對進行變更的連結進行更新。 請注意，檔案上的屬性會反映到該檔案的每個永久連結，而該檔案的屬性變更會傳播到所有的永久連結。 例如，如果您重設永久連結上的 READONLY 屬性以刪除該特定的永久連結，且實際檔案有多個永久連結，則您需要從其中一個剩餘的永久連結重設檔案的 READONLY 位，以將檔案和所有剩餘的永久連結回復至唯讀狀態。

例如，在 C：和 D：是本機磁片磁碟機的系統中，而 Z：是對應到 fred 共用的網路磁碟機機 \\ \\ \\ ，則會允許下列參考作為硬連結：

-   C： \\ dira \\ethel.txt 連結到 c： \\ dirb \\ dirc \\lucy.txt
-   D： \\ dir1 \\tinker.txt 至 d： \\ dir2 \\ dirx \\bell.txt
-   C： \\ diry \\ bob .bak 連結到 C： \\ dir2 \\mina.txt

以下不是：

-   C： \\ dira 連結到 c： \\ dirb
-   C： \\ dira \\ethel.txt 連結至 D： \\ dirb \\lucy.txt
-   C： \\ dira \\ethel.txt 連結至 Z： \\ dirb \\lucy.txt

若要刪除永久連結，請使用 [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) 函數。 您可以依任何順序刪除永久連結，而不考慮它們的建立順序。

## <a name="junctions"></a>接合

*連接* 點 (也稱為「*軟連結*」，) 與硬連結不同，因為它所參考的儲存物件是不同的目錄，而連接點可以連結位於同一部電腦上不同本機磁片區的目錄。 否則，聯接的運作方式與永久連結相同。 連接會透過重新 [分析點](reparse-points.md)來執行。

假設 [永久連結] 區段中的相同條件，則會允許下列參考做為連接：

-   C： \\ dira 連結到 c： \\ dirb \\ dirc
-   C： \\ dirx 連結至 D： \\ diry

以下不是：

-   C： \\ dira \\one.txt 連結到 c： \\ dirb \\two.txt
-   C： \\ dir1 連結至 Z： \\ dir2

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立符號連結](creating-symbolic-links.md)
</dt> </dl>

 

 




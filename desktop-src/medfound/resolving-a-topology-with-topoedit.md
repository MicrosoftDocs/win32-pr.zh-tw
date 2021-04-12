---
description: 使用 TopoEdit 解析拓撲
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: 使用 TopoEdit 解析拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191757"
---
# <a name="resolving-a-topology-with-topoedit"></a>使用 TopoEdit 解析拓撲

拓撲有兩種類型：

-   部分拓撲。 來源節點會直接連接至輸出節點。 在某些情況下，部分拓撲可以有一些中繼轉換節點（例如效果），但並非全部。 略過的轉換節點通常是「解碼器」或「格式轉換 MFTs，例如「色彩轉換器」和「音訊 resamplers」。

-   完整拓撲。 來源節點會透過轉換節點連接至輸出節點。 此類型的拓撲必須具有每個節點，才能處理資料。

TopoEdit 只能播放完整的拓撲。 TopoEdit 會使用媒體基礎所提供的拓撲載入器物件，藉由插入必要的轉換，將部分拓撲轉換成完整拓撲。 建立完整拓撲的程式稱為解析拓撲。

如需拓撲類型的詳細資訊，請參閱 [關於](about-topologies.md)拓撲的「部分拓撲」一節。

在您解決拓撲之前，請確定：

-   拓撲包含來源節點和輸出節點。

-   來源和輸出節點是由有效的節點連接所連接。 在拓撲解析期間，拓撲載入器會檢查節點的媒體類型是否相容。 如果有不正確節點連接，則處理常式會失敗，並顯示錯誤訊息。

若要解決拓撲，請在 [ **拓撲** ] 功能表中，按一下 [ **解析拓撲**]。

工具列會指出拓撲狀態： **\[ 已解決 \]** 或 **\[ 未解決 \]**。

如果 TopoEdit 成功解析拓撲，**拓撲狀態** 會設為 [ **\[ 已 \] 解決**]，並啟用播放控制項。

每次您對拓撲進行變更時，**拓撲狀態** 都會設定為 [ **\[ 未 \] 解決**]，這表示它必須重新解析。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 TopoEdit 建立拓撲](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




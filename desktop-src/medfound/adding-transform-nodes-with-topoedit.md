---
description: 使用 TopoEdit 新增轉換節點
ms.assetid: e1725c37-3f04-4208-9c09-56ce9a854138
title: 使用 TopoEdit 新增轉換節點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97fa39457f8808070f93a4e5de31e181525ca33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318483"
---
# <a name="adding-transform-nodes-with-topoedit"></a>使用 TopoEdit 新增轉換節點

「轉換」節點代表媒體基礎轉換)  (轉換，可處理從來源節點接收的媒體資料。 準備好時，管線會將它傳遞至輸出節點進行轉譯。 在媒體基礎中，編碼器、解碼器、multiplexers、multiplexers 和音訊影片效果都會實作為 MFTs。 TopoEdit 支援加入代表已註冊和自訂 MFTs 的轉換節點。

如需使用媒體基礎 Api 以程式設計方式加入轉換節點的詳細資訊，請參閱 [建立轉換節點](creating-transform-nodes.md)。

## <a name="to-add-a-registered-mft-to-the-topology"></a>將已註冊的 MFT 新增至拓撲

1.  在 [ **拓撲** ] 功能表上，按一下 [ **新增轉換**]。

    [ **選取轉換** ] 對話方塊隨即開啟。 它會顯示已註冊 MFTs 的分類清單，此清單是透過呼叫 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函式來列舉登錄中的已註冊專案所產生。

2.  展開類別，然後選取您要新增至拓撲的 MFT。

3.  按一下 **[確定** ] 關閉對話方塊，並返回 [ **拓撲] 窗格**。

TopoEdit 會建立指定的轉換節點。 [ **拓撲] 窗格** 會將 [轉換] 節點顯示為顯示 MFT 名稱的綠色方塊。

## <a name="to-add-a-custom-mft-to-the-topology"></a>將自訂 MFT 新增至拓撲

1.  在 [ **拓撲** ] 功能表上，按一下 [ **新增自訂 MFT**]。

    這會開啟 [ **輸入自訂 GUID** ] 對話方塊。

2.  在 [ **GUID：** ] 欄位中，輸入您要新增至拓撲的 MFT GUID。

    > [!Note]  
    > TopoEdit 會預期格式為 "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" 的 GUID。 否則，它無法新增節點，並會顯示「不正確 GUID」錯誤訊息。

     

3.  按一下 **[確定** ] 關閉對話方塊，並返回 [ **拓撲] 窗格**。

TopoEdit 會建立指定的轉換節點。 [ **拓撲] 窗格** 會將 [轉換] 節點顯示為顯示 MFT 名稱的綠色方塊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 TopoEdit 建立拓撲](building-topologies-by-using-topoedit.md)
</dt> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




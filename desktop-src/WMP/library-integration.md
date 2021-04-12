---
title: 程式庫整合
description: 程式庫整合
ms.assetid: 6ff1b379-983b-4cd7-8142-27523a7a03e7
keywords:
- Windows Media Player 線上商店、程式庫整合
- 線上商店，程式庫整合
- 輸入1個線上商店，程式庫整合
- Windows Media Player 線上商店、工作窗格
- 線上商店、工作窗格
- 輸入1個線上商店、工作窗格
- Windows Media Player，工作窗格
- Windows Media Player 程式庫，整合
- 程式庫，整合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5353aba7099acd2dfd08596be7ffd43503bdad91
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374483"
---
# <a name="library-integration"></a>程式庫整合

Windows Media Player 的使用者介面會組織成功能區，稱為工作 *窗格*，可封裝程式的各種高階功能。 其中包括連結 **庫**、 **同步** 處理和 **燒錄** 工作窗格 (其他) 。 [連結 **庫** ] 工作窗格可讓使用者使用程式庫;[ **同步** 工作] 窗格可讓使用者將數位媒體檔案同步到可攜式裝置;[ **燒錄** 工作] 窗格可讓使用者將數位媒體檔案燒錄到 CD 或 DVD。

> [!Note]  
> [連結 **庫** ] 工作窗格有時稱為 [ **流覽** 工作窗格]。

 

這些工作窗格中的每一個都有一些與程式庫的整合層級。 例如，如果使用者想要將音樂燒錄至 CD，讓使用者藉由流覽程式庫並直接將媒體專案拖放至清單中，選擇要燒錄的音樂是合理的。 這表示使用者可以在連結 **庫**、 **同步** 處理和 **燒錄** 工作窗格時，查看並使用已完全整合至程式庫的線上商店目錄。 [WMPTaskType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptasktype)列舉包含的值代表這三個工作窗格，因此可以透過程式設計方式加以識別。

這三個工作窗格中的每一個都分成三個主要部分。 第一個部分是程式庫樹狀檢視控制項。 此控制項可讓使用者以階層方式顯示 Windows Media Player 程式庫，包括依歌曲、演出者、專輯等分類功能。 第二個工作窗格部分是 [詳細資料] 窗格。 這個窗格會根據 [程式庫] 樹狀檢視中目前選取的類別，提供詳細的資訊組織。 例如，如果使用者已按一下樹狀檢視中的 [ **歌曲** ]，[詳細資料] 窗格會顯示目前在文件庫中的歌曲標題，以及其他資訊，例如 [長度] 和 [專輯標題]。 第三個部分是 [清單] 窗格或 [ *購物籃*]。 使用者可以將媒體專案拖放到購物籃上，以建立清單，例如播放清單、同步清單和燒錄清單。

當線上商店目錄與程式庫整合時，線上商店會顯示為 [程式庫] 樹狀檢視控制項中的最上層類別或 *節點*。  (一次只能有一位使用者看到一個線上商店目錄。 ) 當使用者按一下節點來選擇觀看線上商店目錄時，[詳細資料] 窗格會顯示線上商店目錄中音樂的相關資訊。 這包括使用者已購買或出租的音樂，以及使用者尚未取得的音樂。

最上層的線上商店節點有一組由 Windows Media Player 提供的子節點。 例如，最上層的線上商店節點有收音機、演出者和專輯子節點，還有其他節點。 最上層的線上商店節點最多可以有8個線上商店提供的自訂子節點。 Windows Media Player 會針對清單識別碼在0到7範圍內的任何清單建立自訂的子節點。 線上商店會在 [list.csv](list-csv.md) 檔案中指定屬於存放區類別目錄的清單識別碼。

Windows Media Player 會呼叫 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)，並在 *bstrInfoName* 參數中傳遞 CPListIDIcon，以抓取每個線上商店的自訂樹狀節點的圖示。

當使用者流覽目錄時，Windows Media Player 會呼叫 **IWMPContentPartner：： GetItemInfo** ，以從內容合作夥伴外掛程式取得使用者所選取之音樂專案的中繼資料。 此中繼資料會提供資訊給播放程式，讓播放程式可以顯示類別目錄專案的詳細資料。 例如，如果使用者選取專輯，Windows Media Player 會抓取專輯封面 URL，讓使用者可以看到專輯封面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於類型1線上商店**](about-type-1-online-stores.md)
</dt> </dl>

 

 





---
title: Windows 7 之後的重要變更，以確保相容性
description: Windows 7 之後的重要變更，以確保相容性
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ed00dacb0d8556d4e16de84fbc20b7ac6a56bed6560bee3213c7919b9760cbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815188"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a>Windows 7 之後的重要變更，以確保相容性

我們了解對於開發人員來說，相容性非常重要。 ISV 與開發人員希望確保他們的 app 可在所有支援的 Windows 作業系統版本上如預期般運作。 消費者與企業的主要投資在這裡—他們希望確保他們付費使用的 app 可以持續運作。 我們了解相容性是採購決策的主要條件。 以最佳作法撰寫的應用程式，在發行新的 Windows 版本時，會導致程式碼變換變得更少，而這些應用程式將可減少分散的工程投資，並加快上市時間。

在 Windows 7 時期，是以非常被動的方式處理相容性問題。 在 Windows 8 中，我們開始以不同的觀點，在 Windows 內盡力確保在設計時便將相容性納入考量，而非在事後補救。 Windows 10 是到目前為止最符合「透過設計提供相容性」的 OS 版本。 以下是我們達成這項目標的主要方法：

-   應用程式遙測：這可協助我們瞭解 Windows 生態系統中的應用程式熱門程度，以通知相容性測試。
-   ISV 合作關係：直接與外部合作夥伴合作，為他們提供資料並協助修正使用者體驗的問題。
-   設計審核：上游偵測：與功能小組合作，減少 Windows 中的重大變更數目。 相容性檢閱是功能小組必須通過的門檻。
-   更嚴密地控制 API 變更 & 改良的通訊
-   試驗和意見反應迴圈： Windows 測試人員人口會收到 flighted 組建，以協助改善在將最終組建發行給客戶之前，尋找相容性問題的能力。 這個意見反應程序不僅能揭露錯誤，也確保我們推出的是使用者想要的功能。

 

 





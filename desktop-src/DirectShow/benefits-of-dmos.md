---
description: DMOs 的優點
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: DMOs 的優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187533"
---
# <a name="benefits-of-dmos"></a>DMOs 的優點

DMOs 提供下列優點：

-   它們通常比 DirectShow 篩選器更小且更簡單，因為它們支援較少的功能。
-   它們比 DirectShow 篩選更有彈性，因為它們不需要篩選圖形。 當您需要 DirectShow 提供的服務時（例如同步處理、智慧型連接、資料流程的自動處理和執行緒管理），您可以使用它們搭配 DirectShow。 不需要這些服務的用戶端可以直接存取 DMOs。
-   DMOs 一律會執行同步資料處理，以消除您撰寫篩選時必須考慮的許多執行緒問題。
-   不同于傳統的 BC-VCM-LVM-HYPERV 編解碼器，DMOs 是以元件物件模型 (COM) 為基礎，因此可以透過 **QueryInterface** 延伸。
-   DMOs 支援比或 BC-VCM-LVM-HYPERV 編解碼器更一般化的串流模型。 就像 DirectShow 篩選器一樣，DMOs 可以支援多個輸入和多個輸出。

基於這些理由，現在建議使用 DMOs 作為撰寫編碼器、解碼器和音訊效果的解決方案。 您也可以視應用程式的需求而定，其他許多案例也是可行的。

DMOs 與 DirectShow 濾波器有何不同

DirectShow 篩選器無法在 DirectShow 篩選圖形之外運作。 在 DirectShow 中，篩選圖形管理員會在應用程式和篩選器之間協調。 DirectShow 篩選器會執行串流資料所需的大部分工作，包括：

-   配置緩衝區。
-   協調媒體類型和連接至其他篩選器。
-   透過篩選圖形推送資料。
-   將事件傳送至篩選圖形管理員。
-   同步處理多個執行緒。

相反地，一說，每一種事都沒有。 相反地，這些類型的工作是用戶端使用 SQL-DMO 的責任。 用戶端會配置緩衝區，並將資料填滿，然後將它們傳遞給該。 SQL-DMO 會處理資料，而用戶端會抓取產生的輸出緩衝區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DMOs](about-dmos.md)
</dt> </dl>

 

 




---
description: DMOs 的優點
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: DMOs 的優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b13a9ef7f91446d03732b935648b689ab65a33c9d10dcfca26051d9284404db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103368"
---
# <a name="benefits-of-dmos"></a>DMOs 的優點

DMOs 提供下列優點：

-   因為它們支援的功能較少，所以通常會比 DirectShow 的篩選器更小且更簡單。
-   它們比 DirectShow 濾波器更有彈性，因為它們不需要篩選圖形。 當您需要 DirectShow 提供的服務（例如同步處理、智慧型連接、資料流程的自動處理和執行緒管理）時，您可以搭配 DirectShow 使用它們。 不需要這些服務的用戶端可以直接存取 DMOs。
-   DMOs 一律會執行同步資料處理，以消除您撰寫篩選時必須考慮的許多執行緒問題。
-   不同于傳統的 BC-VCM-LVM-HYPERV 編解碼器，DMOs 是以元件物件模型 (COM) 為基礎，因此可以透過 **QueryInterface** 延伸。
-   DMOs 支援比或 BC-VCM-LVM-HYPERV 編解碼器更一般化的串流模型。 如同 DirectShow 篩選，DMOs 可支援多個輸入和多個輸出。

基於這些理由，現在建議使用 DMOs 作為撰寫編碼器、解碼器和音訊效果的解決方案。 您也可以視應用程式的需求而定，其他許多案例也是可行的。

DMOs 與 DirectShow 濾波器有何不同

DirectShow 篩選準則無法在 DirectShow 篩選圖形之外運作。 在 DirectShow 中，篩選 Graph 管理員會在應用程式和篩選器之間協調。 DirectShow 篩選準則會執行串流資料所需的大部分工作，包括：

-   配置緩衝區。
-   協調媒體類型和連接至其他篩選器。
-   透過篩選圖形推送資料。
-   將事件傳送至篩選 Graph 管理員。
-   同步處理多個執行緒。

相反地，DMO 不會執行這些動作。 相反地，這些類型的工作是用戶端使用 DMO 的責任。 用戶端會配置緩衝區，並將資料填入資料，並將它們傳遞至 DMO。 DMO 會處理資料，而用戶端會抓取產生的輸出緩衝區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DMOs](about-dmos.md)
</dt> </dl>

 

 




---
title: RPC NDR 格式字串
description: 遠端程序呼叫 (RPC) NDR 格式字串。
ms.assetid: 9c83a039-49d3-491d-8110-29d1548730de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a481e2c992f3fd4dda2d5552fbbabb7e9b01e6eb639a092e25ba9a26bd59a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926302"
---
# <a name="rpc-ndr-format-strings"></a>RPC NDR 格式字串

## <a name="ndr-engine-32-bit-interpreter"></a>NDR 引擎：32位解譯器

本檔說明32位 NDR 引擎的格式字串描述項，有時也稱為 MOPs。 本節說明從 [**– Oi**](/windows/desktop/Midl/-oi) 解譯器到 **– Oif** 解譯器層的演進，以及管道和非同步支援的相關新增專案的變更。

本檔說明目前的 Microsoft 介面定義語言 (MIDL) 技術，從引擎的觀點來看，以及目前的 NDR 引擎。

## <a name="overview"></a>概觀

NDR 引擎是遠端程序呼叫的封送處理引擎， (RPC) 和 DCOM 元件。 它會處理遠端呼叫的所有存根相關問題。 在處理過程中，NDR 封送處理是由 MIDL 產生的存根、MIDL JIT 類型產生器，或由其他工具產生的存根或手動寫入的存根所驅動。 接著，NDR 引擎會驅動與特定傳輸通訊 (DCOM 或 RPC) 的基礎執行時間。

設計的原始目標是要根據 MIDL 編譯器所提供的資訊，提供可有效封送處理任意資料的工具。 本檔所描述的格式字串（以及編譯器針對 NDR 引擎耗用量所產生的所有資訊），一律都被視為編譯器與引擎之間的內部介面。 同樣地，可供引擎用來處理執行時間問題的介面也大多是內部 (在 RPC 執行時間端有一些例外狀況，而引擎使用的一些 DCOM 介面是外部) 。

有兩種常見的封送處理方法，一直都是內嵌和資料驅動的 () 技術來解讀。 MIDL 在其 C 產生的存根中透過其 [**– Os**](/windows/desktop/Midl/-os)和 [**– Oi \***](/windows/desktop/Midl/-oi)參數支援。 此外，MIDL 也可以產生 oleautomation 封裝所使用的 TLB 程式庫。 因此，引擎內部的其中一種觀點是由兩個部分所組成。

第一個是處理調整大小、封送處理等的常式，其對應至一般資料類型物件（例如結構或陣列）。 這些常式可針對效能進行微調;例如，它們通常會盡可能地嘗試封鎖複製資料。 這部分通常稱為「核心 NDR 引擎」。

第二個部分是由解譯器和其相關的部分所組成。 解譯器會使用來自核心 NDR 引擎的常式，就像從內部程式庫一樣，為了執行遠端呼叫，並適當地封送處理和取消封送處理其所有引數。

無論是從內嵌存根還是從解譯器使用，核心的 NDR 引擎都會以類似的方式使用。 所有核心引擎常式都取決於存根訊息結構所傳入的狀態。 結構會由內嵌存根或解譯器適當地設定。 多年來，核心引擎已在不同的內容中使用;目前解譯器實際上是一組數個相異解譯器迴圈。 這些與舊的和新的 ([**– Oi**](/windows/desktop/Midl/-oi) 和 **-Oif**) 解譯器相關，以及與資料序列化相關的迴圈 (pickling) 、RPC 非同步支援和 DCOM 非同步支援 (rpc 和 dcom 有不同的非同步程式設計模型) 。

除了新增功能之外，NDR 引擎演進的重要層面是解譯器方法的一般轉變。 NDR 1.1 版會在新的 MIDL 2.0 方法中開始進行封送處理，並針對效能考慮偏好內嵌存根。 使用最新版本的 NDR， [**-Oif**](/windows/desktop/Midl/-oi) 已成為最廣泛使用的編譯器模式，幾乎是排除內嵌存根。

RPC NDR 引擎格式字串描述項將在下列主題中更詳細地說明：

-   [格式字串](format-strings.md)
-   [程式格式字串](procedure-format-strings.md)
-   [程式標頭描述元](procedure-header-descriptor.md)
-   [處理](handles.md)
-   [標頭](the-header.md)
-   [參數描述項](parameter-descriptors.md)
-   [類型格式字串](type-format-strings.md)

 

 
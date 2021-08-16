---
description: 通訊通常牽涉到可能有大量資料或未知長度的資料。
ms.assetid: e7b12b9e-8caa-4dad-b81f-b609ccb92c9f
title: 使用 SecBufferDesc 和之 secbuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ad12120414a1e0acb7a6b1cfe211b0ed1787d9e676e8329df1e16ecfef17cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785908"
---
# <a name="using-secbufferdesc-and-secbuffer"></a>使用 SecBufferDesc 和之 secbuffer

通訊通常牽涉到可能有大量資料或未知長度的資料。 在這兩種情況下，傳送和接收資料是以類似或相同的方式來完成。 為了處理未知長度和可能的大量資料，SSPI 通訊會使用兩個結構 [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) 和 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)來完成。

[**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc)結構是 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)結構陣列的容器。 **SecBufferDesc** 結構具有下列成員：

-   版本號碼
-   [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)元素的數目
-   [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)結構陣列的位址

[**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)結構包含下列三個成員：

-   緩衝區中的位元組數目
-   資料項目中包含的資訊類型
-   位元組本身

整個 SSPI 訊息通常是由 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) 結構的陣列所組成。

下列緩衝區資料類型的定義如下。



| 緩衝區類型                | 意義                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| 之 SECBUFFER \_ 空白           | 未定義，由 [*安全性封裝*](../secgloss/s-gly.md) 函式取代 |
| 之 SECBUFFER \_ 資料            | 封包資料                                                                                                                            |
| 之 SECBUFFER \_ TOKEN           | 安全性權杖                                                                                                                         |
| 之 SECBUFFER \_ PKG \_ PARAMS     | 封裝特定參數                                                                                                            |
| \_遺漏之 SECBUFFER         | 遺漏資料指標                                                                                                                 |
| 之 SECBUFFER \_ 額外           | 額外的資料                                                                                                                             |
| 之 SECBUFFER \_ 資料流程          | 安全性資料流程資料                                                                                                                   |
| 之 SECBUFFER \_ 資料流程 \_ 結尾 | 安全性資料流程尾端                                                                                                                |
| 之 SECBUFFER \_ 資料流程 \_ 標頭  | 安全性資料流程標頭                                                                                                                 |



 

您可以使用位 **or** 運算搭配下列其中一個緩衝區類型來結合上述緩衝區類型。



| 緩衝區類型         | 意義                                                                          |
|---------------------|----------------------------------------------------------------------------------|
| 之 SECBUFFER \_ ATTRMASK | 藉由分隔屬性旗標與緩衝區類型來遮罩安全性屬性。 |
| 之 SECBUFFER \_ READONLY | 緩衝區是唯讀的                                                              |



 

在每次呼叫需要 [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) 參數的 SSPI API 之前，會宣告並初始化一或多個 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) 陣列元素。 例如，可以有兩個安全性緩衝區：一個包含輸入訊息資料，另一個則用於安全性封裝所傳回的輸出不透明安全性權杖。 安全性緩衝區描述項中的安全性緩衝區順序並不重要，但每個緩衝區都必須以其適當的類型標記。 唯讀標記可搭配 [*安全性封裝*](../secgloss/s-gly.md)不可修改的任何輸入緩衝區使用。

預期包含安全性權杖的輸出緩衝區大小是很重要的。 在初始設定期間，應用程式可以找到安全性封裝的權杖大小上限。 對 [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) 的呼叫會傳回安全性封裝資訊的指標陣列。 安全性套件資訊結構包含每個封裝的權杖大小上限。 在此範例中，資訊位於 [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa)結構的 **cbMaxToken** 成員中。 您可以稍後使用 [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa)取得相同的資訊。

應用程式會初始化緩衝區描述中的緩衝區指標和大小，以指出可以找到訊息資料和其他資訊的位置。

如需詳細資訊，請參閱 [之 secbuffer 和 SecBufferDesc 範例程式碼](secbuffer-and-secbufferdesc-example-code.md)。

 

 

---
title: 介面 Proxy 檔案
description: 介面 proxy 檔案 (U \_ p. c) 是 c 檔案，其中包含的常式相當於用戶端 stub 中的常式和物件 (COM) 介面中的伺服器 stub 檔案。
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL 和 COM MIDL、介面、proxy 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedb9de50d00524b1e038f027448be5aaab369aa5d92243d2a3425bf603cd65a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013536"
---
# <a name="the-interface-proxy-file"></a>介面 Proxy 檔案

介面 proxy 檔案 (U \_ p. c) 是 c 檔案，其中包含的常式相當於用戶端 stub 中的常式和物件 (COM) 介面中的伺服器 stub 檔案。 這個檔案包含在編譯器的內嵌模式中，用戶端和伺服器的代理常式的執行方式，或在解讀模式中的對等資料和 Thunk，以及其他適當的 COM 粘附資料（例如 proxy 和存根 Vtable）。

介面 proxy 檔案僅包含目前 IDL 檔案中所定義介面之方法的支援常式和資料。 若要明確說明這種行為，請在本節中使用擴充的範例。 當編譯具有繼承自 IFaceA 之介面（例如 IFaceB）的 IDL 檔案時，會將 IFaceB 相關的輔助資料和常式產生至目前的 proxy 檔案，而基底介面 IFaceA 相關輔助資料和常式則是在包含 IFaceA 定義的 IDL 檔案所產生的 proxy 中找到。 編譯器會產生識別基底介面之代理程式的所有必要資料，並在需要時將其委派給它們，以支援透過 IFaceB 介面所使用的 IFaceA 方法。

針對目前 IDL 檔案中介面內的每個方法，在混合模式中編譯時，proxy 檔案會包含下列兩個代理方法 ([/os](-os.md)) ，而在解譯器模式中編譯時則對等解譯器資料 ([/Oi](-oi.md)) 。

-   用戶端代理，例如 \_ \_ 此範例中的 IFaceB 方法 Proxy。

    此用戶端代理是用戶端（例如 IFaceB：： Method）分派的虛擬進入點。 它會將輸入引數封送處理成可形式、將封送處理的引數連同識別介面和作業的資訊一起傳送，然後在叫用的作業傳回時，拆收傳回值和任何輸出引數。

-   伺服器端代理，例如 IFaceB \_ 方法 \_ Stub。

    此伺服器端代理是基礎執行時間在伺服器上分派給的虛擬進入點，用以模擬用戶端。 它會拆收輸入引數以複寫用戶端資料、叫用伺服器的介面函式執行，然後將傳回值和任何輸出引數封送處理並傳送回用戶端。

從檔案產生之 proxy 檔案的預設名稱。 .idl 是 file \_ p. c. 使用 [**/proxy**](-proxy.md) MIDL 編譯器參數覆寫介面 proxy 檔案的預設名稱。 [**/Env**](-env.md)和 [**/out**](-out.md)參數會影響這個檔案。

 

 





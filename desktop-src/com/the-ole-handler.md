---
title: OLE 處理常式
description: OLE 處理常式是一個 DLL，其中包含數個用於連結和內嵌的互動元件。
ms.assetid: 5a01b4be-38cf-4019-ba20-ee67b836a3e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9579f18b44a36a794ff807d9d616dd3a06dd1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021519"
---
# <a name="the-ole-handler"></a>OLE 處理常式

*OLE 處理常式* 是一個 DLL，其中包含數個用於連結和內嵌的互動元件。 為了避免容器與其伺服器之間的固定處理序間通訊，會將處理常式載入容器的進程空間，以代表伺服器作為代理程式的一種方式來執行動作。 OLE 處理常式會管理不需要注意伺服器應用程式的容器要求，例如繪圖的要求。 當容器要求物件處理常式無法提供的內容時，處理常式會使用 COM 跨進程通訊機制與伺服器應用程式進行通訊。

OLE 處理常式元件包含遠端處理元件，可管理處理程式和其伺服器之間的通訊、儲存物件資料的快取 (以及如何格式化和顯示該資料) 的相關資訊，以及可協調 DLL 其他元件活動的控制物件。 此外，如果物件是連結，DLL 也會包含連結元件或 *連結的物件*，以追蹤連結來源的名稱和位置。

OLE 提供了一個預設的處理常式，大部分的應用程式都使用這些處理常式來連結和內嵌 如果預設值不符合伺服器的需求，您可以完全取代預設處理常式，或使用它在適當時提供的部分功能。 在後者的情況下，應用程式處理常式會實作為由新控制項物件和預設處理常式組成的匯總物件。 組合應用程式/預設處理常式也稱為同 *進程處理* 程式。 *遠端處理處理常式* 用於未在系統登錄中指派 CLSID 或沒有指定處理常式的物件。 這些物件類型的處理常式所需的全部都是在整個進程界限之間傳遞資訊。 若要建立預設處理常式的新實例，請呼叫 [**OleCreateDefaultHandler**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler)。 在某些特殊情況下，請呼叫 [**OleCreateEmbeddingHelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper)。

當您為某個類別建立處理常式的實例時，您不能將它用於另一個類別。 用於複合檔案時，當您從遠端存取特定類別的物件時，OLE 處理常式會執行容器端資料結構。

OLE 定義了複合檔案本機伺服器用戶端的預設處理常式。 預設處理常式會執行一般伺服器不會執行的一些介面。 當 OLE 之後允許複合檔案的同進程伺服器時，他們必須建立內嵌協助程式來執行這些額外的介面，讓用戶端可以順暢地使用它們。

定義和執行用戶端處理常式的架構設計人員應該在其設計中考慮這個問題，而且應該為相同的原因提供同等的同進程 helper。 即使設計工具目前未在伺服器不公開的處理常式上執行介面，它們仍可能想要立即定義協助程式，以便日後可以加入。 或者，您可以在伺服器物件本身上執行額外的介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[輕量 Client-Side 處理常式](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 





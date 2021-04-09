---
description: 設計 COM + 應用程式的基本指導方針
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: 設計 COM + 應用程式的基本指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111045"
---
# <a name="basic-guidelines-for-designing-com-applications"></a>設計 COM + 應用程式的基本指導方針

若要充分利用 COM +，您可以在建立應用程式時使用幾個基本指導方針：

-   **使用您選擇的資料庫工具，將您的持久狀態模型為資料庫架構。** 幾乎每個應用程式都必須維持持久狀態。 資料庫會提供建立持久且可調整的狀態儲存區所需的服務。 因此，建立 COM + 應用程式的第一個步驟是將應用程式的持久狀態模型為某種資料庫架構。 您所使用的資料庫並不重要，大部分的商務資料庫都與 COM + 相容。 Microsoft SQL Server 是一個可供您使用的解決方案的絕佳範例。

-   **將 COM + 應用程式的邏輯模型為一組 COM 介面。** 當您的架構表示應用程式的狀態資訊之後，就會將應用程式中發生的交換模型為 COM 介面。 這些介面會建立應用程式行為的模型。 當您應判斷哪些 COM + 服務最適合您的應用程式時，這也是開發階段。

-   **建立元件 Dll，其中包含使用實體資料結構描述的元件，並將資料的邏輯觀點公開 (給此清單中的第一個專案) ，以及在邏輯資料模型中所實行的元件， (此清單) 的第二個專案。** 當您擁有邏輯的結構和狀態資訊之後，就可以開始撰寫程式碼，而且現在可以撰寫以 DLL 為基礎的 COM 元件，這些元件會根據定義的架構來執行介面。 您的元件只是用來處理資料庫資訊的操作工具，而且您的元件 Dll 可讓您建立可正常運作且可順利調整的 COM + 應用程式。

-   **使用您所選取的 COM + 服務，在 COM + 環境中部署元件。** 建立應用程式之後，您就可以在網路或伺服器叢集上部署應用程式。 您現在可以根據可用的資源進行決策，並可為每個元件量身打造以獲得最大效能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 設計假設和原則](com--design-assumptions-and-principles.md)
</dt> <dt>

[使用 UML 設計 COM + 應用程式](designing-the-com--application-using-uml.md)
</dt> <dt>

[使用 COM + 的一般設計秘訣](general-design-tips-for-using-com-.md)
</dt> <dt>

[優化與 COM + 商務邏輯層的互動](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[用來建立分散式應用程式的其他 Microsoft 工具](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 




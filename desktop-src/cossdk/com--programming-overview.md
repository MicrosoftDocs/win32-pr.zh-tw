---
description: COM + 會根據 Microsoft 元件物件模型 (COM) 來提供企業開發環境，以建立以元件為基礎的分散式應用程式。
ms.assetid: 141982d4-1e6c-4f01-8b0e-8b94f20dd82c
title: COM + 程式設計總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c225b5ebb6f04f74d6071dc0305d219993fa606e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688715"
---
# <a name="com-programming-overview"></a>COM + 程式設計總覽

COM + 會根據 Microsoft 元件物件模型 (COM) 來提供企業開發環境，以建立以元件為基礎的分散式應用程式。 它也提供您建立交易式多層式應用程式的工具。 COM + 透過許多實用的程式設計和管理服務，將增強功能與傳統的 COM 型開發結合在一起。 如需這些服務的完整清單，請參閱 [Com + 服務](com--services.md) 。

COM 增強功能包含執行緒和安全性的增強功能，以及同步處理服務的引進。 這些服務包括「元件服務」系統管理工具。

針對熟悉 COM 程式設計的人，COM + 的改進很重要，包括下列各項：

-   COM + 會實作為中立的單元執行緒的執行緒模型，讓元件能夠有序列化的存取，以及在任何執行緒上執行的能力。
-   COM + 支援具有特殊環境的元件，稱為 [內容](com--contexts.md)，它提供了一組可定義元件執行環境的可延伸屬性。
-   COM + 提供以角色為基礎的安全性、非同步物件執行和內建的名字標記，代表在跨進程伺服器上執行的物件實例的參考。

## <a name="application-and-component-administration"></a>應用程式和元件管理

在 COM + 中，名為 RegDB 的註冊資料庫會儲存描述元件的中繼資料。 此資料庫經過高度優化，適用于 COM + 啟動元件時所需的資訊類型，而且會用來取代系統登錄。 此外，COM + 會公開 *Com + 類別目錄*，以存取 RegDB 中的資訊。 COM + 類別目錄是系統資料存放區，其中包含指定伺服器電腦上 COM + 應用程式的設定資訊。

最後，「元件服務」系統管理工具提供可完整編寫腳本的使用者介面，讓開發人員和系統管理員管理元件，以及部署用戶端和伺服器端多層式應用程式。 如需詳細資訊，請參閱 [部署 COM + 應用程式](deploying-com--applications.md)。

## <a name="automatic-transactions"></a>自動交易

COM + 支援所有的 Microsoft Transaction Server (MTS) 2.0 的語義，並新增 [自動完成](enabling-auto-done-for-a-method.md) 功能，您可以使用 [元件服務] 系統管理工具來設定此功能。 這項功能可讓系統在觸發例外狀況或認可時自動中止交易。 如需詳細資訊，請參閱 [Com + 交易](com--transactions.md)和 [Com + 即時啟用](com--just-in-time-activation.md)。

 

 




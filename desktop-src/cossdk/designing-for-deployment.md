---
description: 設計部署
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: 設計部署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468109"
---
# <a name="designing-for-deployment"></a>設計部署

規劃 COM + 應用程式的範圍是您應該提早考慮的重要設計工作。 使用 COM + 執行的分散式系統應設計為具有最少個別設定的部署，以及最有效率地使用每個進程。 您也可以使用這些技術，讓您在部署 COM + 應用程式時達到最佳效能。  (需詳細資訊，請參閱 [部署以加快通訊速度](deploying-for-faster-communication.md)) 

使用 [元件服務] 系統管理工具來查看時，每個 COM + 應用程式都會顯示為一個資料夾，其中包含以邏輯方式分組的元件集。 雖然您可以在 COM + 應用程式 **元件** 資料夾之間移動個別元件 (換句話說，從某個應用程式到另一個) ，在 com + 應用層級（例如安全性）設定的數個服務可能會不同。 這些服務設定可能會影響可攜性。

## <a name="a-com-server-application-defines-a-process-boundary"></a>COM + 伺服器應用程式定義進程界限

當您建立新的 COM + 伺服器應用程式時，您實際上是定義新的進程界限。  (記下以下說明的程式庫應用程式例外狀況。 ) 此程式會成為 COM + 應用程式中所包含元件的控制應用程式實例。 當程式第一次呼叫 COM + 應用程式時，這些元件都會在 COM + 可執行程式的新實例中執行同進程。 這表示指定的 COM + 應用程式 **元件** 資料夾內的所有元件都是在作為 DCOM 伺服器的單一進程空間中執行。 在 COM + 應用程式中，COM + 會管理記憶體、與分散式交易協調器 (DTC) 、及時元件實例啟用、損毀偵測和復原，以及以角色為基礎的安全性。

## <a name="calling-across-com-application-boundaries"></a>跨 COM + 應用程式界限呼叫

因為每個 COM + 應用程式通常會實作為個別可執行檔，所以將分散式應用程式分割成多個 COM + 應用程式的影響會在某個 COM + 應用程式中的元件呼叫另一個 COM + 應用程式中的元件時，引進跨進程 COM 呼叫。 這會導致效能降低，因為跨進程的封送處理 COM 參數會產生額外的負擔。

> [!Note]  
> 造成此效能的影響不會發生任何問題，您只需要知道，就會發生這種情形。 根據所需的回應時間、將同時要求商務服務的使用者數目，以及每個元件新增到每個 COM + 應用程式的額外啟動負擔，您可能會發現可接受對跨應用程式呼叫造成的效能衝擊。

 

消除跨 COM + 應用程式界限呼叫之效能損失的其中一種可能性，是將指定的 COM + 應用程式標示為程式庫應用程式。 COM + 程式庫應用程式是在建立它的用戶端的進程中執行。 當然，不會有任何效能提升的成本。 在此情況下，取捨牽涉到 COM + 程式庫應用程式的限制。 雖然程式庫應用程式可以使用以角色為基礎的安全性，但它無法支援已排入佇列的元件或遠端存取。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[部署以加快通訊速度](deploying-for-faster-communication.md)
</dt> <dt>

[可用性設計](designing-for-availability.md)
</dt> <dt>

[擴充性設計](designing-for-scalability.md)
</dt> <dt>

[安全性設計](designing-for-security.md)
</dt> </dl>

 

 




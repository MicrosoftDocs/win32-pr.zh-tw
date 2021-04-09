---
description: 概念模型：應用程式需求
ms.assetid: 124b329b-f745-45b4-b266-7c177c76a5cd
title: 概念模型：應用程式需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a287ff940f154bf104bbb50f6362bf573d9223
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111020"
---
# <a name="the-conceptual-model-application-requirements"></a>概念模型：應用程式需求

設計概念模型時，您需要定義商務問題以及解決這些問題所需的功能。 最佳做法是與實際使用應用程式的人員討論、與廣大的使用者見面，以及盡可能納入最多的商務或使用者案例。 判斷系統可能使用者的身分識別和數量，以及相關資料的大小與範圍。 雖然收集這項資訊可能是設計流程中最不的技術層面，但這是最重要的一環。 若要開發成功的應用程式，您需要清楚瞭解需要解決的商務問題和流程。

判斷應用程式需求時，請記住下列考慮：

-   效能需求。 應用程式工作的預期回應時間為何？ 需要關閉伺服器的容錯移轉支援？ 有哪些小時的可用性？
-   環境。 有哪些伺服器可供使用？ 是否已規劃其他伺服器來處理任何調整需求？
-   部署。 應用程式將如何與目前的系統整合？ 應用程式會與其他系統互動嗎？ 其他系統所使用的作業系統有哪些？ 應該支援哪些通訊協定？ 您可以使用哪個 API 來與其他系統互動？ 其他系統位於網路上的何處？ 電腦使用的限制有哪些？ 允許存取哪些使用者帳戶？
-   位置。 相對於用戶端的資料位於何處？ 資料是從遠端存取，還是在本機？
-   安全性。 是否有加密或完整性檢查需求？ 是否有驗證或資料保護需求？
-   存取權限。 誰有權執行特定作業的條件約束？ 如果是，您應該先記錄哪些作業需要授權，然後記載可擁有授權的使用者類型。 這些需求可能會對應用程式的各個部分的執行方式造成很大的影響。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[邏輯模型：應用程式定義和規劃](the-logical-model--application-definition-and-planning.md)
</dt> <dt>

[實體模型：應用程式架構](the-physical-model--application-architecture.md)
</dt> </dl>

 

 




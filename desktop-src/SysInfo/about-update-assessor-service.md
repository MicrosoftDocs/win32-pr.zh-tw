---
description: 下列主題說明 Windows 即服務 (WaaS) 評量平臺 API 的運作方式。
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: 關於 WaaS 評定平臺
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79493900d508a8a613953f1f9b7bbd0f67e2a200761148b7fe31d9fb31ce3609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117958948"
---
# <a name="about-the-waas-assessment-platform"></a>關於 WaaS 評定平臺

下列主題說明 Windows 即服務 (WaaS) 評量平臺 API 的運作方式。

WaaS 評量 API 會將下列資訊提供給呼叫者：

-   如果裝置位於最新的 Microsoft 更新。
-   裝置是否已達到終止支援。
-   裝置最新適用更新的發行時間。
-   評量裝置不是最新狀態的原因，以及可能對裝置造成的潛在影響。

WaaS 評估平臺會使用 COM API 模型，而且每天至少會自動執行一次。 此迴圈會捕捉適用的發行資訊。 在快取期間，會對快取的版本資訊進行評量。 如果在快取到期時間範圍外進行呼叫，就會建立並快取並傳回新的呼叫和評量。 進行呼叫時，WaaS 評估用戶端會將 WaaS 評量服務與裝置的屬性連線，並接收適用于裝置的資訊 dossier。 然後，用戶端會使用此資訊，根據它針對裝置所收集的資訊來執行評量。

> [!NOTE]
> 您的程式碼必須具有系統管理員許可權，才能呼叫 Waas 評定 API。 如需有關開發需要系統管理員許可權之應用程式的詳細資訊，請參閱 [這篇文章](../secauthz/developing-applications-that-require-administrator-privilege.md)。

 

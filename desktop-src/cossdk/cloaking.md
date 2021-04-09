---
description: 有兩個因素可決定模擬的行為：用戶端會透過模擬等級明確授與伺服器的授權，以及在用戶端上呼叫用戶端時，能夠遮罩自己的身分識別。
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: " (元件服務的掩蔽) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688719"
---
# <a name="cloaking-component-services"></a> (元件服務的掩蔽) 

有兩個因素可決定模擬的行為：用戶端會透過模擬等級明確授與伺服器，以及在代表用戶端進行呼叫時，讓伺服器能夠遮罩自己的身分識別。 後者的功能稱為 *掩蓋*。 掩蓋必須利用伺服器進行呼叫所使用的安全性識別。

當伺服器模擬用戶端時，它可以直接存取用戶端的安全性認證。 在本機上，伺服器執行緒會採用用戶端的身分識別。 但是，當伺服器在其進程之外進行呼叫時，不一定會將用戶端身分識別投射為進行呼叫時所用的身分識別。

啟用「遮蓋」時，您可以透過用戶端的身分識別，在模擬用戶端的伺服器上進行呼叫。 停用遮蓋時，伺服器的呼叫會在伺服器的身分識別下進行。

此外，也有兩種形式的掩蓋、 *靜態的掩蓋* 和 *動態掩蓋*，如下所述：

-   使用靜態掩蓋進行模擬。 原始用戶端身分識別 (發現為伺服器執行緒權杖，) 可以使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)在呼叫上向下游伺服器顯示一次，並在 proxy 上設定一次原始用戶端識別，而該執行緒權杖將用於後續的方法呼叫。
-   使用動態掩蓋進行模擬。 在對下游伺服器的每個方法呼叫上，會將原始用戶端身分識別視為伺服器執行緒 token。 實際上，提供的身分識別可動態判斷。 進行此作業所需的額外負荷可能會大幅增加。

針對 COM + 應用程式，預設設定為動態掩蓋功能。 這可以透過程式設計的方式和系統管理員來變更。 雖然動態擬呼可能會有效能額外負荷，但它提供的彈性通常是需要先使用模擬的情況。

如需有關可能行為之掩蓋和精確描述的詳細資訊，請參閱 COM 檔中的「 [掩蔽](/windows/desktop/com/cloaking) 」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端模擬和委派](client-impersonation-and-delegation.md)
</dt> <dt>

[模擬的用戶端需求](client-side-requirements-for-impersonation.md)
</dt> <dt>

[模擬的伺服器端需求](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 

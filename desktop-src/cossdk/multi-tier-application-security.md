---
description: 多層式應用程式安全性
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: 多層式應用程式安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ba43970c2af5ff6c7abb733767b721091f6a3d3407178d5360e5f96db11d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070467"
---
# <a name="multi-tier-application-security"></a>多層式應用程式安全性

在資料庫中，您可以在決定要于多層式元件型應用程式中強制執行安全性的情況下，面對困難的選擇： 在中介層？ 在元件中嗎？ 別處？ 到處？ 隨著安全性機制的數量和複雜性增加，效能會降低，而應用程式行為會變得更不容易預測。 不過，您必須確保資料受到保護、遵循商務規則，以及記錄重要的活動，而且您的應用程式仍可在預期的情況下為用戶端工作。 您必須確定透過應用程式的每個用戶端路徑都正確無誤，而且您備妥的安全性檢查點也足夠。

最困難的決策通常是要在資料庫上強制執行安全性。 在過去，這就是安全性嚴謹的地方，因為它被認為是一台需要真正安全的那個，而且資料庫管理員很不願意信任其他人來強制執行安全性。 但是，在資料庫上強制執行安全性可能相當昂貴，而且很難調整規模，而這是一開始撰寫多層式應用程式的重點。

使用 COM + 進行可擴充的多層式應用程式要遵循的一般規則，可能的話，您應該盡可能在中介層的 COM + 應用程式中強制執行詳細的安全性。 這樣做可讓您充分利用 COM + 所提供的可擴充服務。 只有在您絕對需要時才在資料庫上進行驗證，並且完全衡量這麼做的效能含意。

如需決定要在何處執行安全性檢查的相關問題討論，請參閱 [決定要](deciding-where-to-enforce-security.md)在哪裡強制執行安全性檢查。

如需保護多層式應用程式之基本案例的討論，請參閱 [在多層式應用程式中保護資料的基本案例](basic-scenarios-for-securing-data-in-multi-tier-applications.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端驗證](client-authentication.md)
</dt> <dt>

[用戶端模擬和委派](client-impersonation-and-delegation.md)
</dt> <dt>

[程式庫應用程式安全性](library-application-security.md)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> <dt>

[以角色為基礎的安全性管理](role-based-security-administration.md)
</dt> <dt>

[在 COM + 中使用軟體限制原則](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 




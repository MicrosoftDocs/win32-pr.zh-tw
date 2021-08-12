---
description: 已排入佇列的元件安全性
ms.assetid: 3fbeb81a-e3e4-495b-b891-896877fab92f
title: 已排入佇列的元件安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682a9b409df2f605c259a6af6741dcc6e59d9fc23852b950a13225b24386c010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547080"
---
# <a name="queued-components-security"></a>已排入佇列的元件安全性

當用戶端對已排入佇列的物件呼叫方法時，實際上會對記錄器進行呼叫，這會將它封裝成訊息的一部分。 接聽程式會從佇列讀取訊息，並將它傳遞給播放程式。 Player 會叫用實際的伺服器元件，並進行相同的方法呼叫。 當 player 進行方法呼叫時，伺服器元件必須觀察用戶端的安全性呼叫內容 (而不是播放程式的安全性呼叫內容) 。 錄製器會將用戶端的安全性呼叫內容封送處理到訊息中，然後播放程式會在伺服器上拆收它，然後再進行方法呼叫。 就伺服器物件而言，直接呼叫用戶端與播放程式的間接呼叫之間的安全性內容沒有任何差異。 尤其是，叫用的方法會以寄件者的許可權執行。

COM + 佇列元件支援以角色為基礎的安全性語義，就像是為了與 COM + 應用程式一起使用而建立的其他元件一樣。 因此，佇列應用程式的元件可以使用程式設計介面，來探索其呼叫端的角色成員資格 ([**ISecurityCallCoNtext：： IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) 或特定使用者 ([**ISecurityCallCoNtext：： IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)) 。 建議任何有潛在安全性影響的已排入佇列元件，都使用這些介面明確檢查寄件者的認證。

呼叫端身分識別是與方法呼叫相關聯的身分識別。 以角色為基礎的安全性會使用呼叫端身分識別，並存在於安全性呼叫內容中。 在已排入佇列的元件中，呼叫端身分識別會表示為訊息佇列訊息中的資料。 訊息佇列會驗證訊息寄件者身分識別。 當呼叫端身分識別和訊息寄件者身分識別相同時，訊息佇列會驗證訊息和呼叫端。 這是一般情況。

> [!Note]  
> COM + 佇列的元件不支援模擬樣式的安全性，可讓伺服器取得對應至用戶端身分識別的存取權杖，並使用它來執行存取控制檢查或在用戶端安全性內容下採取動作。

 

當已排入佇列之元件的呼叫端透過跨進程的錄製器與元件互動時，呼叫端的身分識別和訊息傳送者 (記錄器) 可能會不同。 在此情況下，COM + 佇列的元件會確認訊息寄件者是伺服器上的「QC 信任的使用者」角色的成員。 此外，跨進程記錄器需要驗證憑證，因為它是由訊息佇列進行驗證。

QC 信任的使用者角色的成員可以指定任意的識別碼，這表示惡意的成員可以利用較高的權限來執行佇列元件呼叫。 因此建議將這類使用者的數目保持在絕對最少數。

因為有一項複雜的攻擊與任何機制（會在網路上傳播身分識別）相關聯，以及透過 unexecutable 要求而產生簡單阻絕服務攻擊的風險，所以建議您只在受信任主機的網路上部署 COM + 佇列的元件服務，例如： 在私人網路或虛擬私人網路中，或在適當設定的防火牆後方。

COM + 佇列元件會透過 DCOM 執行，因此您可以在佇列應用程式的 [內容]**工作表的**[**安全性**] 索引標籤上，選取 [封 **包隱私權**] 作為 [**呼叫的驗證等級**] 設定，以協助保護佇列方法呼叫的完整性和機密性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 安全性](com--security.md)
</dt> <dt>

[工作組模式中的安全性限制](security-limitations-in-workgroup-mode.md)
</dt> <dt>

[指定驗證通訊協定](specifying-the-authentication-protocol.md)
</dt> </dl>

 

 




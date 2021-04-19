---
description: 擴充功能可讓應用程式以線性方式增加資源使用量來服務額外的負載。
ms.assetid: 8249f1af-9c96-4545-ad6a-3736c6e63c6d
title: 擴充性設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ab0aa9d67afaac14c6d8f59df34183bde36113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970910"
---
# <a name="designing-for-scalability"></a>擴充性設計

擴充功能可讓應用程式以線性方式增加資源使用量來服務額外的負載。 在任何分散式應用程式中，擴充性都很重要。 擴充性的限制通常會在應用程式的設計中，以資源使用和不小心建立的相依性為中心。

下列清單說明擴充性問題並建議解決方案：

-   電腦內部資源。 可用的執行緒和記憶體數目可以限制擴充性。 針對您的應用程式使用最有效率的執行緒模型。
-   電腦間資源。 散發應用程式工作負載的可用電腦數目可能會影響擴充性。
-   用戶端親和性。 應用程式可能會不慎建立兩種親和性的情況：應用程式相依于用戶端隨其要求傳送的資料狀態;以及應用程式需要用戶端特定狀態的情況。 避免在用戶端與應用程式之間設計狀態相依性。
-   伺服器親和性。 COM + 應用程式可以藉由建立伺服器親和性來限制其擴充性，而應用程式相依于前往特定的伺服器電腦以取得相關資訊。 許多資料庫導向應用程式可能會發生這個親和性。 避免伺服器親和性瓶頸的最佳方式，就是將資料分割到各種伺服器電腦上。 例如，根據最常存取的金鑰將客戶資料分割在不同的伺服器上，或使用客戶的姓氏將客戶資料庫跨越數部伺服器 (例如 Server1： a-f、Server2： g-m、Server3： n-z) 。
    > [!Note]  
    > 資料分割可以在程式設計邏輯中增加很多複雜性，而且只有在嘗試增加擴充性的其他選項之後才應完成。

     

-   物件存留期。 COM + 應用程式必須密切注意物件的存留期，才能進行擴充。 當物件存在時，就會耗用資源。 請務必確定保存到昂貴資源之物件的存留期是謹慎管理的。 針對不耗用昂貴資源的高需求物件， [Com + 物件](com--object-pooling.md) 共用可以增加擴充性，因為您可以系統管理員調整共用值，以利用您可能擁有的任何硬體。 這是控制連接的自然方式：例如，如果您有20個 SQL 連接的授權，您可以使用 [最大集區] 設定來指定。
-   應用程式元件群組。 為了增強 COM + 應用程式的擴充性，中介層元件應該分成時間相依和與時間無關的服務。 這可讓您專注于可能使用 Microsoft Windows 服務來執行必要的元件動作。 例如，您可以選擇使用 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 或 [com + 佇列元件](com--queued-components.md) 等服務來處理與時間無關的非同步工作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[可用性設計](designing-for-availability.md)
</dt> <dt>

[設計部署](designing-for-deployment.md)
</dt> <dt>

[安全性設計](designing-for-security.md)
</dt> </dl>

 

 




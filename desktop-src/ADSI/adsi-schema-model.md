---
title: ADSI 架構模型
description: 架構類似于字典，因為它會保留目錄服務已知之每個物件類型的定義。
ms.assetid: 70561a11-1560-4b1c-a999-e2a7b2002ab0
ms.tgt_platform: multiple
keywords:
- ADSI 架構模型 ADSI
- ADSI ADSI、about、schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4893151c81eefa0a17420e18d5d87da232641571
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883875"
---
# <a name="adsi-schema-model"></a>ADSI 架構模型

架構類似于字典，因為它會保留目錄服務已知之每個物件類型的定義。 ADSI 用戶端應用程式可以流覽架構，以探索任何指定 ADSI 執行的功能。 此外，ADSI 也提供架構管理介面，可用來與目錄服務的基礎架構進行通訊。

某些架構是可擴充的，且 ADSI 提供者或協力廠商可能會選擇為現有介面發佈新的介面或其他屬性。 ADSI 用戶端會使用此資料來判斷每個目錄服務所支援的功能。

有三種類型的架構物件：類別、屬性和語法，分別支援架構管理介面 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)、 [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)和 [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)。

> [!Note]  
> 類別是多載的詞彙。 有 c + + 類別、JAVA 類別、COM 類別和 ADSI 類別。 在本檔中，除非另有限定，否則 word 類別會參考架構物件的類別或類型。

 

ADSI 會摘要每個目錄服務的架構，並將它放在 **命名空間** 物件中的每個最上層根節點。 若要識別目錄服務在給定根節點上支援哪些類別，您可以列舉架構物件，並取得類別物件、屬性物件和語法物件的清單。 如需詳細資訊，請參閱 [使用 ADSI 架構](using-the-adsi-schema.md)。

## <a name="adsi-ldap-provider-schema-cache"></a>ADSI LDAP 提供者架構快取

ADSI 的 LDAP 提供者會嘗試將架構資料快取到本機電腦。 Ubschema 是以 [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) 屬性中儲存的分辨名稱來識別，位於目錄服務 Enterprise (rootDSE) 的根目錄中。 除了提供 ubschema 資料之外，LDAP v3 伺服器也應該公開 [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) 屬性，以用來判斷上次修改架構的時間。

ADSI 初次系結至 LDAP 伺服器時，會使用 [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) 屬性來抓取 ubschema 的資料。 如果 ADSI 成功尋找 ubschema 物件，它會將資料指標儲存在連線到 LDAP 伺服器之電腦上的登錄中。 如需有關這些值儲存在登錄中的確切資訊，請參閱 [ADSI 和使用者帳戶控制](adsi-and-uac.md)。

ADSI 接著會嘗試處理架構資料並讀取 [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) 屬性。 如果 **modifyTimeStamp** 屬性存在且 adsi 成功處理架構，adsi 會將 ubschema 寫入磁片，並在機碼底下建立兩個下列登錄值。 如果 ubschema 資料存在，但無法處理，則不會建立這些登錄值：

-   **時間** 值，包含 [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp)屬性。 這個值是用來確保架構資料是最新的，並防止架構資料的常數重載。
-   檔案 **值，** 包含 ADSI 將架構資料儲存在檔案系統中的路徑。 根據預設，ADSI 會將 ubschema 快取在 &lt; systemroot &gt; \\ SchCache 目錄中，並以對應至 LDAP 伺服器名稱的檔案名來快取。

如果可處理 ubschema 資料，但未公開 [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) 屬性，則會將架構資料快取在記憶體中，但不會寫入磁片。 如果已透過本機電腦上的 ADSI 連接到 LDAP v3 伺服器，而且快取的 ubschema 不存在，最有可能是下列其中一個原因：

-   伺服器未公開正確的屬性。
-   ADSI 無法處理架構。
-   ADSI 無法將檔案寫入檔案系統。

 

 

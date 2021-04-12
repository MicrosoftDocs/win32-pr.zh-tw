---
description: 若要啟用安裝程式功能，應用程式必須在初始化時呼叫許多函數。
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: 初始化應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192441"
---
# <a name="initializing-an-application"></a>初始化應用程式

若要啟用安裝程式功能，應用程式必須在初始化時呼叫許多函數。 如需詳細資訊，請參閱 [安裝機制](installation-mechanism.md)。 下列步驟說明如何使用安裝程式將應用程式初始化：

**初始化應用程式**

1.  呼叫 [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) 函式，讓應用程式能夠將其本身識別為安裝程式。

    產品代碼是許多安裝程式函數的必要參數。

2.  呼叫 [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) 函式，以在應用程式第一次啟動時收集使用者資訊。

    如果呼叫 [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) 失敗，請呼叫 [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) 函式來收集使用者資訊。

3.  藉由呼叫 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) 函式來顯示預設使用者介面（如有必要）。

    若要撰寫您自己的使用者介面，請呼叫 [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) 函式將其註冊到安裝程式。

4.  呼叫 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) 函數來設定記錄層級。
5.  藉由列舉應用程式的功能，讓使用者擁有可用的功能。 您可以透過下列方式列舉功能：
    -   依功能查詢安裝程式功能。 例如，在應用程式繪製按鈕或功能表項目之前，應用程式會呼叫 [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) 函式，讓安裝程式可以檢查功能是否可用。
    -   藉由呼叫 [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) 函數，一次列舉所有可用的功能。 若要使用此函數，應用程式必須在遞增索引時重複呼叫 **MsiEnumFeatures** 。
6.  若要取得目前安裝的詳細資訊，請重複呼叫下列列舉函數，為每個呼叫遞增索引變數：

    -   呼叫 [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) 函式來列舉向安裝程式註冊的產品。
    -   呼叫 [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) 函數來列舉元件。
    -   呼叫 [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) 函數來列舉元件限定詞。
    -   呼叫 [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) 函數，以列舉特定元件的產品。

    如果列舉函數的傳回值是錯誤 \_ 成功，則會列舉更多專案，而且應該使用遞增的索引變數再次呼叫函式。 如果傳回值 \_ 沒有 \_ 其他 \_ 專案，則會列舉所有的專案，而且不應該再次呼叫該函式。

 

 




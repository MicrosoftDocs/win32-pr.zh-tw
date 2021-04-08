---
description: 預設系統存放區（包括 MY、CA 和 ROOT）會實作為邏輯集合存放區，其中包含許多預先定義的實體存放區做為其成員存放區。
ms.assetid: 1d82b94b-4842-454a-aca4-823cd264ac52
title: 邏輯與實體存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a5441bac91e39b7f4c124daecd3a6a569c323c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690747"
---
# <a name="logical-and-physical-stores"></a>邏輯與實體存放區

預設系統存放區（包括 MY、CA 和 ROOT）會實作為邏輯集合存放區，其中包含許多預先定義的實體存放區做為其成員存放區。 系統存放區的成員實體存放區會在系統存放區開啟時自動開啟。 使用者可以在任何系統存放區集合中新增其他實體存放區。 CryptoAPI 函數 [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore) 會將新的實體存放區加入至系統存放區集合。 [**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore) 會解除實體存放區與邏輯系統存放區的之間的解除。 [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore) 會在登錄 hKey 下建立新的系統存放區，而 [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore) 會從登錄中移除系統存放區。

在 CryptoAPI 中，系統存放區是具有相關聯實體存放區的邏輯存放區。 現有系統存放區中的所有憑證都會保持可用，而實體新增憑證則是在組成邏輯系統存放區的實體存放區中進行。

如果使用者想要繼續使用實體系統存放區，而不是轉換成邏輯存放區，則可以使用 CERT \_ STORE \_ >prov \_ system \_ REGISTRY provider 開啟系統存放區。 此提供者會繼續使用每個系統存放區做為單一實體存放區。

函式 [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation)、 [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)和 [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) 清單系統存放區位置、可用的系統存放區，以及屬於系統存放區成員的所有實體存放區。

系統存放區也可以重新置放。 根據預設，系統會根據預先定義的模式，開啟相對於登錄子機碼的系統存放區。 如需詳細資訊，請參閱 [系統存放區位置](system-store-locations.md)。 \_ \_ \_ \_ 在傳遞至 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)的 *dwFlags* 參數中設定 CERT 系統存放區位置旗標，會將系統存放區放在登錄中使用者指定的登錄子機碼下，而不是預先定義的登錄子機碼。

 

 




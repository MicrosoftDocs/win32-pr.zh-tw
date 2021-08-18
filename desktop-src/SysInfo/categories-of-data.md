---
description: 將資料放入登錄之前，應用程式應該將資料分成兩個類別：電腦特定的資料和使用者特定的資料。
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: 資料類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad4bf4abb7af2abf723aa42f3426c58230083d8e575dda176b8eeda0daecb36d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885849"
---
# <a name="categories-of-data"></a>資料類別

將資料放入登錄之前，應用程式應該將資料分成兩個類別：電腦特定的資料和使用者特定的資料。 藉由進行這項區別，應用程式可以支援多個使用者，還可以透過網路來尋找使用者專屬的資料，並在不同的位置使用該資料，以允許與位置無關的使用者設定檔資料。  (使用者設定檔是一組為每位使用者儲存的設定資料。 ) 

安裝應用程式時，它應該會在 **HKEY \_ 本機 \_ 電腦** 金鑰下記錄電腦特定的資料。 尤其是，它應該建立公司名稱、產品名稱和版本號碼的金鑰，如下列範例所示：

**HKEY \_LOCAL \_ MACHINE \\ Software \\** _MyCompany \\ MyProduct \\ 1.0_

如果應用程式支援 COM，則應該將該資料記錄在 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 下。

應用程式應該在 **HKEY \_ 目前 \_ 使用者** 金鑰下記錄使用者特定的資料，如下列範例所示：

**HKEY \_CURRENT \_ USER \\ Software \\** _MyCompany \\ MyProduct \\ 1.0_

 

 




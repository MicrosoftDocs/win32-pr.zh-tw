---
title: 設定 Microsoft 定位器名稱服務提供者
description: 您可以藉由編輯 Rpcreg .dat 設定檔（其中包含 NSP 參數和 RPC 通訊協定設定）來變更您指定的名稱服務提供者。 使用文字編輯器來變更 NSP 專案。
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 413d7654096b2a7eda74d28b019cac73afe1d0eb182d48d9c0eda601dd2c87c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931603"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a>設定 Microsoft 定位器名稱服務提供者

您可以藉由編輯 Rpcreg .dat 設定檔（其中包含 NSP 參數和 RPC 通訊協定設定）來變更您指定的名稱服務提供者。 使用文字編輯器來變更 NSP 專案。

**若要重新設定 Microsoft 定位器名稱服務提供者**

1.  使用文字編輯器開啟 Rpcreg .dat 檔案。

    除非您在安裝期間指定不同的路徑，否則 Rpcreg 會在根目錄中。

2.  設定登錄專案的下列值。 

    | 登錄項目                                         | 值                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 軟體 \\ Microsoft \\ RPC \\ NameService \\ 通訊協定       | 您正在使用之通訊協定的通訊協定順序。 預設值為 **ncacn \_ np**。                                                                   |
    | Software \\ Microsoft \\ RPC \\ NameService \\ networkaddress.cache.ttl | 在名稱服務查閱作業期間，用戶端所使用之執行定位器的電腦名稱稱。 預設值是主域控制站。 |
    | 軟體 \\ Microsoft \\ RPC \\ NameService \\ 端點       | 名稱服務所使用之端點的名稱。 預設值為 [ \\ 管道 \\ 定位器]。                                                                    |

    

     

3.  儲存並關閉檔案。

 

 





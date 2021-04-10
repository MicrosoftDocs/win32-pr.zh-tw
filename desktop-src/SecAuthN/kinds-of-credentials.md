---
description: 說明認證管理 API 用來處理的兩種認證。
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: 認證類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30968484b2cfc89b9238f624d9299fb75c72bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944415"
---
# <a name="kinds-of-credentials"></a>認證類型

認證管理 API 適用于兩種類型的認證：

-   [網域認證](#domain-credentials)
-   [一般認證](#generic-credentials)

## <a name="domain-credentials"></a>網域認證

作業系統會使用網域認證，並由「本地安全機構」 (LSA) 進行驗證。 一般來說，當註冊的安全性套件（例如 Kerberos 通訊協定）驗證使用者所提供的登入資料時，就會建立使用者的網域認證。 系統會快取登入認證，讓單一登入可讓使用者存取許多不同的資源。 例如，網路連線可能會以透明的方式進行，而且可以根據使用者的快取網域認證來授與受保護系統物件的存取權。

認證管理功能提供一種機制，讓應用程式在使用者登入之後提示使用者輸入網域認證，並讓作業系統驗證使用者提供的資訊。

網域認證的秘密部分（密碼）會受到作業系統的保護。 只有使用 LSA 執行同進程的程式碼可以讀取和寫入網域認證。 應用程式僅限於寫入網域認證。

Windows 支援擴充智慧卡和憑證認證的使用。 為了協助確保安全性，認證管理 API 永遠不會將智慧卡 PIN 儲存在電腦上。

## <a name="generic-credentials"></a>一般認證

一般認證是由直接管理授權和安全性的應用程式所定義和驗證，而不是將這些工作委派給作業系統。 例如，應用程式可以要求使用者輸入應用程式提供的使用者名稱和密碼，或產生 [*憑證*](../secgloss/c-gly.md) 來存取網站。

應用程式會使用認證管理功能來提示使用者提供應用程式定義的一般認證資訊，例如使用者名稱、憑證、智慧卡或密碼。 使用者輸入的資訊會傳回給應用程式進行驗證。

認證管理提供可自訂的快取管理和一般認證的長期儲存。 使用者進程可以讀取和寫入一般認證。

 

 

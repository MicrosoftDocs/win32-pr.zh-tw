---
description: 使用加密技術來加密公開金鑰、加密演算法、RSA 加密及數位憑證。
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: 密碼編譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050f84d118cb5ad9e1da49ddabd73489745339bb0b1357e229b0f1609a1c997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876108"
---
# <a name="cryptography"></a>密碼編譯

## <a name="purpose"></a>目的

密碼編譯是使用程式碼來轉換資料，如此一來，只有特定的收件者才能夠使用金鑰來讀取它。

Microsoft 密碼編譯技術包括 CryptoAPI、密碼編譯服務提供者 (CSP) 、CryptoAPI 工具、CAPICOM、WinTrust、發行和管理憑證，以及開發可自訂的公開金鑰基礎結構。 此外也會說明憑證和智慧卡註冊、憑證管理和自訂模組開發。

## <a name="developer-audience"></a>開發人員對象

CryptoAPI 適用于以 Windows 為基礎的應用程式開發人員，可讓使用者在安全的環境中建立及交換檔和其他資料，尤其是透過非安全的媒體（例如網際網路）。 開發人員應該熟悉 C 和 c + + 程式設計語言，以及 Windows 程式設計環境。 雖然並非必要，但建議您瞭解密碼編譯或安全性相關的主題。

CAPICOM 是一個僅限32位的元件，可供使用 Visual Basic 腳本撰寫版的開發人員使用 (VBScript) 程式設計語言或 c + + 程式設計語言。 您可以在 Run-Time 需求所指定的作業系統中使用 CAPICOM。 針對未來的開發，建議您使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。

## <a name="run-time-requirements"></a>執行階段需求求

如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。

下列作業系統和版本支援 CAPICOM 2.1.0.2：

-   Windows Server 2003
-   Windows XP

您可以從可從 [PLATFORM SDK](https://www.microsoft.com/download/details.aspx?id=25281)可轉散發套件下載的可轉散發檔案取得 capicom： capicom。

憑證服務需要下列作業系統版本：

-   Windows Server 2008 R2
-   Windows Server 2008
-   Windows Server 2003

## <a name="in-this-section"></a>本節內容



| 主題                                                           | 描述                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於密碼編譯](about-cryptography.md)<br/>         | 重要的密碼編譯概念，以及 Microsoft 加密技術的高階觀點。<br/>                                                                                                                           |
| [使用加密](using-cryptography.md)<br/>         | 使用 CryptoAPI 函式和 CAPICOM 物件的 C 和 Visual Basic 程式的密碼編譯器、程式和擴充的範例。<br/>                                                                            |
| [密碼編譯參考](cryptography-reference.md)<br/> | Microsoft 加密函式、介面、物件、結構和其他程式設計項目的詳細說明。 包含使用數位憑證的 API 參考描述。<br/> |



 

 

 





---
description: CryptoAPI 已設計為可輕鬆擴充。 所有密碼編譯服務提供者都可以定義新的類型和參數， (CSP) 作者，以對各種情況的需求進行 CryptoAPI 折讓。
ms.assetid: fe87ccb8-16a3-443d-93df-0df02b8787f6
title: 擴充 CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62417f66b8a8bb2d06d145543f944f91868d366d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975293"
---
# <a name="extending-cryptoapi"></a>擴充 CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) 已設計為可輕鬆擴充。 所有 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 都可以定義新的類型和參數， (CSP) 作者，以對各種情況的需求進行 CryptoAPI 折讓。



| 可擴充專案                                                                                                 | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 提供者類型<br/>                                                                                        | 提供者類型代表密碼編譯服務的特定系列或類型。 您可以定義新的提供者類型，每個都提供特定的小程式。<br/>                                                                                                                                                                                                                                                                                          |
| 提供者參數<br/>                                                                                   | 提供者參數會分別使用 [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) 和 [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**)來傳送和接收。 新的提供者參數可以讓您以 CryptoAPI 設計工具未預見的方式設定 CSP。<br/>                                                                                                                                                                 |
| 演算法識別碼<br/>                                                                                 | [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**)的列舉功能可讓應用程式動態列出演算法識別碼。 您可以隨時定義新的 [*對稱*](../secgloss/s-gly.md)、 [*公開金鑰*](../secgloss/p-gly.md)和 [*雜湊*](../secgloss/h-gly.md) 演算法。<br/> |
| 公開/[*私密金鑰*](../secgloss/p-gly.md) 組類型<br/> | 雖然可以視需要定義新的金鑰組類型，但目前只會使用簽章和金鑰 [*交換金鑰*](../secgloss/e-gly.md) 組。<br/>                                                                                                                                                                                                                                           |
| 金鑰 BLOB 類型<br/>                                                                                        | 新的金鑰 [*BLOB*](../secgloss/b-gly.md) 類型可允許使用 [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) 和 [**CPImportKey**](https://www.bing.com/search?q=**CPImportKey**) 功能，以彈性的方式交換工作階段金鑰、公開金鑰和公開/私密金鑰組。<br/>                                                                                                                                            |
| 金鑰參數<br/>                                                                                        | 系統會使用 [**CPSetKeyParam**](https://www.bing.com/search?q=**CPSetKeyParam**) 和 [**CPGetKeyParam**](https://www.bing.com/search?q=**CPGetKeyParam**)來傳送和取出金鑰參數。 新的金鑰參數可以支援許多不同類型的金鑰。<br/>                                                                                                                                                                                                                         |
| 雜湊物件參數<br/>                                                                                | 雜湊物件參數會使用 [**CPSetHashParam**](https://www.bing.com/search?q=**CPSetHashParam**) 和 [**CPGetHashParam**](https://www.bing.com/search?q=**CPGetHashParam**)來傳送和取出。 新的雜湊物件參數可以支援許多不同類型的 [*雜湊*](../secgloss/h-gly.md)。<br/>                                                                                                                                         |
| 旗標值<br/>                                                                                           | 大部分的 CryptoAPI/CryptoSPI 函數都有 *dwFlags* 參數。 新的 *dwFlags* 值可以視需要修改函式的行為。<br/>                                                                                                                                                                                                                                                                                                       |



 

CryptoAPI 的延伸模組必須以負責任的方式進行。 在定義新的參數和演算法類型之前，CSP 開發人員應該查閱 Microsoft Corporation，以便：

-   您可以識別一般 CryptoAPI 延伸模組，並將其放入標準的 Wincrypt .h 檔案中。
-   可以避免命名空間衝突。
-   您可以判斷是否需要延伸模組，或是否可使用目前的 API 來達成特定的作業。

> [!Note]  
> 為了讓 CSP 與針對 Microsoft 基礎密碼編譯提供者開發的應用程式相容，它必須支援 [基礎密碼編譯功能](cryptography-functions.md) 和 [密碼編譯服務提供者](cryptography-functions.md)函式中所述的所有前述專案。

 

 

 

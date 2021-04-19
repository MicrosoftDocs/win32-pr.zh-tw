---
description: 憑證註冊控制項可供必須要求將憑證發行至已命名主體的應用程式使用。
ms.assetid: ce6661b0-7ed2-452f-a54c-6705d14f3298
title: 憑證註冊控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e417a9db7984cbb58b7c2e3b51d828b6d61a97b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971195"
---
# <a name="certificate-enrollment-control"></a>憑證註冊控制項

憑證註冊控制項可供必須要求將憑證發行至已命名主體的應用程式使用。 它是設計來接受二進位字串格式的資料， (BSTR) 。 資料可能來自于網頁，或是來自 Visual Basic 或 Visual C++ 開發系統的使用者介面。 憑證註冊控制項的輸出是 PKCS \# 10 憑證要求，可 (CA) 傳送給 [*憑證授權單位*](../secgloss/c-gly.md) 單位。

![憑證註冊控制項](images/xen-arch.png)

有關使用者的必要資訊（憑證主體）是由消費者介面所收集。 這項資訊是以 BSTR 輸入的形式提供給憑證註冊控制項。 憑證註冊控制項會產生適當的簽章金鑰、金鑰交換金鑰或這兩個金鑰組。 然後，控制項會 \# 使用產生的 [*私密金鑰*](../secgloss/p-gly.md)來產生和簽署 PKCS 10 [*憑證要求*](../secgloss/c-gly.md)。 憑證註冊控制項會將金鑰組連結至暫存的虛擬憑證，該憑證會儲存在要求存放區，直到從憑證授權單位單位傳回發行的憑證為止。 最後，應用程式會將 PKCS \# 10 憑證要求傳送給 CA。

如果 CA 核准憑證要求，CA 就會建立包含公開金鑰的憑證。 CA 也會簽署並傳回憑證。

從 CA 傳回所要求的憑證時，應用程式會將 PKCS \# 7 訊息傳回給憑證註冊控制項，其中憑證或憑證鏈會從 PKCS \# 7 訊息解壓縮。 憑證和信任鏈中的任何其他憑證都會儲存在 [*憑證存放區*](../secgloss/c-gly.md)中。 傳回的憑證不會以任何方式修改。 任何憑證感知的應用程式現在都可以從存放區存取此憑證。

系統管理員會使用智慧卡註冊控制來代表智慧卡使用者進行註冊。 註冊程式會導致發行的憑證儲存在使用者的智慧卡上。

智慧卡註冊控制項包含在 Scrdenrl.dll 中，其中包含一個 **SCrdEnr** 的物件。 Scrdenrl.dll 中不包含其他物件。 此智慧卡註冊物件可以與指令碼語言搭配使用，例如 Visual Basic Scripting Edition (VBScript) 。

執行智慧卡註冊控制項的電腦上必須安裝 [*智慧卡讀卡機*](../secgloss/r-gly.md) 。

此外，智慧卡簽發者必須取得以 "EnrollmentAgent" 憑證範本為基礎的簽署憑證。 此簽署憑證將用來代表智慧卡收件者簽署產生的憑證要求。 根據預設，網域系統管理員會被授與根據「註冊代理程式」範本要求憑證的許可權。 另一位使用者也可以透過 Active Directory 網站和服務 MMC 嵌入式管理單元) ，授與註冊「EnrollmentAgent」憑證 (的許可權;不過，這樣做可讓這位使用者使用網域系統管理員許可權自行發出智慧卡。

 

 

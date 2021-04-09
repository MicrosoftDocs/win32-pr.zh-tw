---
description: 封裝程式碼是識別特定 Windows Installer 套件的 GUID。
ms.assetid: dcb6a0d4-e28d-453d-9bda-bfe74f74579b
title: 封裝碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14aa77dbc6c11a1b420572293669a4177f7845ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115356"
---
# <a name="package-codes"></a>封裝碼

封裝程式碼是識別特定 Windows Installer [*套件*](p-gly.md)的 GUID。 封裝程式碼會將 .msi 檔案與應用程式或產品產生關聯，也可以用於驗證來源。 產品和套件代碼不可互換。 如需詳細資訊，請參閱 [產品代碼](product-codes.md)。

Nonidentical .msi 檔案不能有相同的封裝程式碼。 變更封裝程式碼很重要，因為它是安裝程式用來搜尋並驗證指定安裝之正確封裝的主要識別碼。 如果在未變更套件程式碼的情況下變更套件，安裝程式仍可存取安裝程式時，安裝程式可能不會使用較新的套件。

封裝程式碼會儲存在 [摘要資訊資料流程](summary-information-stream.md)的 [[**修訂編號摘要**](revision-number-summary.md)] 屬性中。 請注意，產品代碼和套件程式碼 Guid 中的字母必須為大寫。 GUIDGEN 之類的公用程式會產生包含小寫字母的 Guid。 這些 Guid 中的小寫字母必須變更為大寫，才能當做產品代碼或封裝程式碼使用。

雖然傳送具有相同封裝程式碼和產品程式碼的應用程式很常見，但在更新應用程式時，這兩個值可能會分離出來。 例如，包含應用程式的新檔案需要更新安裝資料庫以安裝檔案。 如果變更較小，開發人員可能會選擇不變更產品代碼，不過，需要不同的 .msi 檔案才能安裝新的檔案，因此封裝程式碼必須遞增。 相反地，您可以使用單一套件來安裝多項產品。 例如，在沒有語言轉換的情況下安裝套件，可以安裝英文版的應用程式，而且使用語言轉換安裝相同的套件可能會安裝法文版。 轉換與決定封裝程式碼的 .msi 檔不同。 英文和法文版本可能會有不同的產品代碼和相同的封裝碼，因為兩者都是使用相同的 .msi 檔案來安裝。

 

 




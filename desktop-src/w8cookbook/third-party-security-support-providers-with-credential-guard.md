---
title: Credential Guard 和協力廠商應用程式
description: Credential Guard 不允許協力廠商 SSP 向 LSA 要求密碼雜湊。
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5c773379e3b7fa52e2095d8db676dddc081e51806fd8f615d2b3a4b744fea95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706748"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a>具有 Credential Guard 的協力廠商安全性支援提供者

Credential Guard 不允許協力廠商 SSP 向 LSA 要求密碼雜湊。 不過，當使用者登入及/或變更其密碼時，SSP 和 AP 仍然會取得密碼通知。 不支援在自訂的 SSP 與 AP 內使用任何未記載的 API。

隨著 Credential Guard 所提供之保護的深度和廣度增加，後續搭配執行 Credential Guard 的 Windows 10 版本可能會影響過去可行的案例。 例如，Credential Guard 可能會封鎖特定類型之認證或特定元件的使用，以防止惡意程式碼利用漏洞。 因此，我們建議在將有執行 Credential Guard 的裝置升級之前，先針對組織中操作所需的案例進行測試。

請參閱 [這篇文章](/windows/security/identity-protection/credential-guard/credential-guard) ，以取得完整的說明和建議的防護措施。

 

 
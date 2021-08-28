---
title: 應用程式目錄分割安全性
description: 應用程式目錄分割的安全性與存取控制模型與 Active Directory Domain Services 中的其他分割區相同。
ms.assetid: 3e14b31a-524e-4b38-957f-166e80b35b31
ms.tgt_platform: multiple
keywords:
- 應用程式目錄分割安全性 AD
- 應用程式目錄分割 AD，安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20da5f0c869329637ae6182224cf67e2feb5684491c34534ac80a67f72b795c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024398"
---
# <a name="application-directory-partition-security"></a>應用程式目錄分割安全性

應用程式目錄分割的安全性與存取控制模型與 Active Directory Domain Services 中的其他分割區相同。 一般使用者可以存取應用程式目錄分割中的物件，這些物件會受限於放在這些物件上的 Acl。 如需詳細資訊，請參閱 [控制 Active Directory Domain Services 中的物件存取](controlling-access-to-objects-in-active-directory-domain-services.md)。

不過，由於應用程式目錄分割可以跨目錄服務中的多個安全性網域，因此在應用程式目錄分割中建立物件時，會在物件的架構類別 [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) 中，解釋與網域相關的已知 SID 字串常數的問題。 例如，如果 "DA" 指的是網域系統管理員群組，但在應用程式目錄分割中，則不知道 "DA" 群組所指的是哪個網域。

若要解決這個問題，應用程式目錄分割的 [**交叉**](/windows/desktop/ADSchema/c-crossref) 參考物件具有 [**SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) 屬性，其中包含該應用程式目錄分割之參考功能變數名稱的分辨名稱。 安全性系統使用指定的網域來解讀本機網域參考，以取得附加至該應用程式目錄分割中所建立物件的預設安全描述項。 當建立應用程式目錄分割的 **交叉** 參考物件時，可以指定參考網域。 不過，這需要針對應用程式目錄分割預先建立 **交叉引用** 物件。 如果未指定任何參考網域，系統就會根據下列其中一個條件來自動設定參考網域：

-   如果應用程式目錄分割物件的父系是另一個應用程式目錄分割，則會將父應用程式目錄分割的 [**SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) 屬性用於參考網域。
-   如果父物件是網域，則會將該網域用於參考網域。
-   如果沒有父物件，則會使用樹系根域作為參考網域。

建立分割區之後， **交叉** 參考屬性也可以變更為參考定義域，但不建議這樣做。

如果在應用程式目錄分割中的物件 ACL 中指定了本機群組，就會發生類似的問題。 在此情況下， [**SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) 屬性不能用來解讀本機群組的參考網域。 若要避免這個問題，請不要在應用程式目錄分割物件的 Acl 中使用本機群組。

 

 
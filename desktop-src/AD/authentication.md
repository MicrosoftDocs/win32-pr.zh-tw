---
title: '驗證 (AD DS) '
description: Active Directory Domain Services 中的每個物件都有唯一的安全描述項，可定義讀取或更新物件或其個別屬性所需的存取權限。
ms.assetid: a4a663d3-b0f3-4993-a74e-9e4f896e8c95
ms.tgt_platform: multiple
keywords:
- Active Directory、using、binding、authentication
- 系結驗證廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80bbca4604a99011d3198eaf6b3e871cd3f84c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462936"
---
# <a name="authentication-ad-ds"></a>驗證 (AD DS) 

Active Directory Domain Services 中的每個物件都有唯一的安全描述項，可定義讀取或更新物件或其個別屬性所需的存取權限。 存取權限是由授與使用者帳戶或群組成員資格的許可權所決定。

當應用程式系結至目錄中的物件時，應用程式對該物件所擁有的存取權限會以系結作業期間指定的使用者內容為基礎。 針對系結函式和方法 [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject)、 [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject)、 **GetObject**、 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject)，應用程式可以隱含地使用呼叫端的認證、明確指定使用者帳戶的認證，或使用未經驗證的使用者內容 (Guest) 。

 

 
---
description: 當用戶端開始時，它會針對其與伺服器的交易選取安全性封裝，然後再與該伺服器連線。 伺服器會選取一或多個安全性套件，並等候用戶端連接。
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: 取得安全性封裝的相關資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626b5bf53ddc9ef20f0110dc7695a7245245604ca9e11baa3cbb50b2c1bd393f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883098"
---
# <a name="getting-information-about-security-packages"></a>取得安全性封裝的相關資訊

當用戶端開始時，它會針對其與伺服器的交易選取 [*安全性封裝*](/windows/desktop/SecGloss/s-gly) ，然後再與該伺服器連線。 伺服器會選取一或多個安全性套件，並等候用戶端連接。

如需特定 SSP 可用之 SSPI 安全性封裝的特定資訊，可以呼叫 [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) 函數來取出 [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) 結構。

為了取得輸出結構，呼叫端會將指標的位址傳遞至函式，以指向傳回結構的型別。 此函式會配置記憶體，並藉由將傳回資料緩衝區的位址指派給引數，來將資料傳回給呼叫者。 SSPI 慣例是函式會為結構配置記憶體，而呼叫的應用程式則會使用 [**FreeCoNtextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer)來釋放該記憶體。

呼叫 [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) 函式會捕獲 [*安全性封裝*](/windows/desktop/SecGloss/s-gly)的屬性。 伺服器和用戶端都可以呼叫 **QuerySecurityPackageInfo** 函數，從 [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa)結構的 **cbMaxToken** 成員取得安全性權杖的最大長度。 如需範例，請參閱 [使用 SSPI 搭配 Windows 通訊端伺服器](using-sspi-with-a-windows-sockets-server.md)中所示的 **QuerySecurityPackageInfo** 函式的呼叫。

如需封裝函數的詳細資訊，請參閱 [套件管理](authentication-functions.md)。

 

 

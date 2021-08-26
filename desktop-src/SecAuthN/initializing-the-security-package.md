---
description: 列出並說明初始化安全性封裝所需的步驟。
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: 初始化安全性封裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d39cbbd9a1126a22d04c14bee3b6ac9b305b2feb3593d03756779e4cb0649b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015848"
---
# <a name="initializing-the-security-package"></a>初始化安全性封裝

使用 SSPI 之前，必須執行下列步驟：

1.  您必須呼叫初始化函式，才能取得安全性函式資料表的位址。

    [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea)分派資料表指標的用戶端和伺服器呼叫 [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) 。 此資料表包含在 Sspi 中宣告之回呼函式的指標。 這些指標可讓您存取各種 SSPI 函式的 DLL 實作為。

2.  您必須取得有關支援之安全性封裝的資訊。

    雖然大部分的應用程式都使用支援預設或一般功能的安全性封裝，但安全性套件可能具有應用程式所需的獨特功能。 需要特殊功能的應用程式可以使用提供這些功能的套件。 如需詳細資訊，請參閱 [取得安全性封裝的相關資訊](getting-information-about-security-packages.md)。

此時，應用程式已成功將 SSP 初始化，並選擇具有足夠功能的安全性封裝。

您可以在用戶端與伺服器之間，使用可在幕後使用哪一個 [*安全性封裝*](../secgloss/s-gly.md)進行 [*協商*](../secgloss/n-gly.md)的合約套件。 如果未使用 Negotiate 套件，用戶端和伺服器必須同意特定安全性封裝，才能執行上述設定步驟。

 

 

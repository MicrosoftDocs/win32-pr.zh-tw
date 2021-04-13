---
description: 安全性支援提供者介面 (SSPI) 可讓應用程式使用電腦或網路上提供的各種安全性模型，而不需要變更安全性系統的介面。
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: SSPI 模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386071"
---
# <a name="sspi-model"></a>SSPI 模型

[*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) 可讓應用程式使用電腦或網路上提供的各種安全性模型，而不需要變更安全性系統的介面。 SSPI 不會建立登入 [*認證*](../secgloss/c-gly.md) ，因為這通常是作業系統所處理的特殊許可權作業。

[*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 包含在 [*動態連結程式庫*](../secgloss/d-gly.md) (DLL) ，藉由將一或多個 [*安全性套件*](../secgloss/s-gly.md)提供給應用程式來執行 SSPI。 每個安全性套件都會提供應用程式的 SSPI 函式呼叫與實際安全性模型的功能之間的對應。 安全性套件支援 [*Kerberos*](../secgloss/k-gly.md)驗證和 LAN Manager 等 [*安全性通訊協定*](../secgloss/s-gly.md)。

SSPI 介面可在核心模式和使用者模式中使用。 若要在核心模式中使用 SSPI 功能，您必須安裝 Windows 可安裝的檔案系統 DDK。 呼叫模型保持不變，但在函數參考頁面上會注明核心模式考慮。 如需詳細資訊，請參閱 [SSPI 函數](authentication-functions.md)。

 

 

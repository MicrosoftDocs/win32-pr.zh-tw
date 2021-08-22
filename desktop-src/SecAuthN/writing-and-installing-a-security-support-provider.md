---
description: SSPI 的設計可讓您撰寫其他 Ssp 並將其新增至系統。
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: 撰寫和安裝安全性支援提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac7125c386314ec7772a5e6079f423af0aaf5c9f7dd820a24c042d99834d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914747"
---
# <a name="writing-and-installing-a-security-support-provider"></a>撰寫和安裝安全性支援提供者

SSPI 的設計可讓您撰寫其他 Ssp 並將其新增至系統。 您可以根據與作業系統的整合層級，以相對較簡單或很大的複雜度來開發安全性模型專屬的 [*SSP*](../secgloss/s-gly.md) 。 允許連接到新類型伺服器的用戶端 SSP 可以非常快速地進行開發，而提供本機模擬的完整 SSP 需要更多投入時間。

您可以藉由更新登錄中的 **REG \_ SZ** 值來安裝 ssp，如下所示：

**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **>hklm\system\system\currentcontrolset\control\securityproviders\schannel\protocols\tls**  =  *Provider1.dll，Provider2.dll，*.。。    <dl> <dt>

            Data type
</dt> <dd>            REG \_ SZ</dd> </dl>

單一 DLL 可以包含多個 Ssp。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊和安裝安全性套件的限制](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 

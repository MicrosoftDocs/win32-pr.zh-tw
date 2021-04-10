---
description: 在開發安全性支援提供者/驗證套件動態連結程式庫 (SSP/AP DLL) 包含一或多個自訂安全性封裝之後，您必須加以註冊。
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: 註冊 SSP/AP Dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692924"
---
# <a name="registering-sspap-dlls"></a>註冊 SSP/AP Dll

在開發 [*安全性支援提供者*](../secgloss/s-gly.md) / [*驗證套件*](../secgloss/a-gly.md)動態連結程式庫 (SSP/AP DLL) 包含一或多個自訂 [*安全性封裝*](../secgloss/s-gly.md)之後，您必須加以註冊。 若要這樣做，請將自訂 SSP/AP DLL 的名稱新增至下列登錄值的資料：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制** \\ **Lsa** \\ **安全性封裝**

此登錄值的資料為不含 ".dll" 副檔名的 SSP/AP Dll 名稱清單。 這份清單的資料類型為 **REG \_ 多重 \_ SZ** ，因此 \\ 清單中每個 DLL 名稱之間必須有 null 字元 ( ' 0 ' ) 。

通常，SSP/AP Dll 會儲存在% systemroot%/system32 目錄中。 如果這是您自訂 SSP/AP DLL 的路徑，則不會將路徑包含為 DLL 名稱的一部分。 但是，如果 DLL 位於不同的路徑中，請在名稱中包含 DLL 的完整路徑。

每次系統啟動時，LSA 都會載入這份清單中的 SSP/AP Dll，並執行 [LSA 模式初始化](lsa-mode-initialization.md)中所述的初始化順序。

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a>註冊自訂安全性套件作為預設的 TLS SSP

在開發自訂的 TLS 安全性支援提供者，並如上面所述註冊之後，您也必須將它註冊為「預設的 TLS SSP」。 若要這樣做，請將自訂 SSP 的封裝名稱填入下列登錄值的資料中：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制** \\ **Lsa** \\ **預設 TLS SSP**

此登錄值的資料是 SSP 的封裝名稱，而不是 dll 名稱。 這種類型的資料類型是 **REG \_ SZ**。

使用「預設 TLS SSP」的使用者模式應用程式將會使用此處註冊的預設值。 使用「Microsoft 統一安全性通訊協定提供者」或其他特定 TLS SSP 名稱的核心模式應用程式或使用者模式應用程式不會受到這項變更的影響。

> [!Note]  
> 此登錄資訊僅適用于 SSP/AP DLL。 如需 (Ssp) 註冊安全性支援提供者的詳細資訊，請參閱 [撰寫和安裝安全性支援提供者](writing-and-installing-a-security-support-provider.md)。 如需有關 SSP/AP 與 SSP Dll 之間差異的詳細資訊，請參閱 [ssp/ap 與](ssp-aps-versus-ssps.md)ssp。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊和安裝安全性套件的限制](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 

---
description: 腳本和 Visual Basic 應用程式必須設定 DCOM 安全性，特別是針對遠端存取，而且可能也需要啟用許可權。
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: 保護腳本用戶端
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192072"
---
# <a name="securing-scripting-clients"></a>保護腳本用戶端

腳本和 Visual Basic 應用程式必須設定 DCOM 安全性，特別是針對遠端存取，而且可能也需要啟用許可權。

## <a name="default-access-permissions"></a>預設存取權限

本機和遠端電腦之間的 WMI 存取不同。 如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。

以下是依帳戶的預設存取權限：

-   每個人、LocalService、NetworkService

    讀取或寫入資料，以及在本機電腦上執行 [*提供者方法*](gloss-p.md) 的許可權。 這些帳戶無法建立新的類別或安裝新的提供者。

-   系統管理員帳戶

    在本機電腦上完全控制。 當連接到遠端電腦時，該帳戶也必須是遠端電腦上的本機系統管理員。

## <a name="securing-a-scripting-client"></a>保護腳本用戶端

WMI 腳本和 Visual Basic 應用程式必須適當地為其設為目標的作業系統設定 DCOM 安全性層級。 如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。

連接到遠端電腦時，您可能需要變更處理驗證 (NTLM 或 Kerberos) 的服務。 如需詳細資訊，請參閱 [使用 VBScript 設定驗證服務](setting-the-authentication-service-using-vbscript.md)。

存取某些 WMI 類別或資料可能需要未啟用的許可權。 例如，連接到 [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) 類別時，您必須包含安全性許可權。 如需詳細資訊，請參閱 [使用 VBScript 執行特殊許可權作業](executing-privileged-operations-using-vbscript.md)。

如果您要從 Active Server Page (ASP) 存取 WMI，則需要進行一些 IIS 設定。 如需詳細資訊，請參閱 [為 WMI ASP 腳本設定 IIS 5.0 和更新版本](configuring-iis-5-for-wmi-asp-scripting.md)。

您可能嘗試連接到需要加密連接的命名空間，換句話說，需要驗證層級的 pktPrivacy。 如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。

 

 

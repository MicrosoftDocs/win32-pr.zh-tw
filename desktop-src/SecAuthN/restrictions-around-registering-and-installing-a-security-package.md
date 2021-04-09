---
description: Windows 不支援之安全性封裝的動作。
ms.assetid: E2BF8041-DF2F-4282-A3CC-A15FF2D7F4A2
title: 註冊和安裝安全性套件的限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd10cd8e2e98d4dccfc3a6230c3daecaeb8fec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689483"
---
# <a name="restrictions-around-registering-and-installing-a-security-package"></a>註冊和安裝安全性套件的限制

收件匣安全性套件的移除、取代或包裝 (例如，在 Windows 中，Kerberos 或 NTLM) 不是支援的動作，而從2017年1月10日起，就會防止它。 您可以新增協力廠商安全性套件 (Ssp/Ap) 不過，Windows 不支援移除預先設定的 Ssp/Ap。 具體而言，不支援編輯 **HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ OSConfig \\ Security 套件** 登錄設定。

從 Windows 8.1 開始，想要提供額外功能的客戶可以使用登錄設定 **HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ LSA \\ SECURITY 封裝** ([註冊 SSP/AP dll](registering-ssp-ap-dlls.md)) 以及相關的登錄設定 **>hklm\system\system\currentcontrolset\control\securityproviders\schannel\protocols\tls** ([撰寫和安裝安全性支援提供者](writing-and-installing-a-security-support-provider.md)) （如果適用的話），來新增安全性封裝。 此外， [安全性套件](../secgloss/s-gly.md#_security_security_package_gly) 的目的是要執行新的 *安全性通訊協定* ，其形式可以是安全性支援提供者 (SSP) 或 (AP) 的 [驗證套件](../secgloss/a-gly.md#_security_authentication_package_gly) 。 SSP 的用途是提供系統中尚未支援的 *已驗證* 連線、 *訊息完整性* 和 *訊息加密服務* ，而使用 AP 來新增 *驗證邏輯* ，用來判斷是否允許使用者登入。

Microsoft 投資客戶的安全性，並嘗試確保不會輕易地從系統移除重要的進程，例如 Ssp 和 Ap。 因此， **HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ OSConfig \\ Security 套件** 登錄設定在 Windows 8.1 中受到限制，以防止變更。 為了加速協力廠商安全性封裝， **HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ Security 封裝** 已成為自訂 ssp/ap 的指定設定。 此外，建議您將自訂的 Ssp/Ap 中的任何功能，從這類自訂 Ssp/Ap 移除，而不是任何產品都移除收件匣安全性套件。

 

 

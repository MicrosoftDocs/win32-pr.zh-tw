---
description: 將每部電腦系統原則的值設定為 &\# 0034; 1&\# 0034;，可讓非系統管理員的使用者從儲存在媒體上的來源（例如 cd-rom）安裝受控應用程式。
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853488"
---
# <a name="allowlockdownmedia"></a>AllowLockdownMedia

將每部電腦 [系統原則](system-policy.md) 的值設定為 "1"，可讓非系統管理員的使用者從儲存在媒體上的來源（例如 cd-rom）安裝 [*受控應用程式*](m-gly.md) 。 請參閱 [來源復原](source-resiliency.md)。 例如，如果設定此原則，則非系統管理員的使用者可能會使用媒體來源來安裝已指派或已發佈的應用程式，或針對所有使用者安裝的應用程式。 設定此原則也可讓非系統管理員的使用者在提高許可權的安裝期間，以 LocalSystem 許可權執行程式。

只有在執行 Windows Vista 且未加入網域的電腦上，此原則的預設值為1。 在其他電腦上的預設值是，非受控使用者無法從位於媒體的來源安裝受控應用程式。

因為此原則可讓非系統管理員的使用者以預設沒有的許可權安裝，所以在設定此原則之前，您應該考慮是否為使用者提供適當的安全性層級。 建議使用預設設定，以確保安全的環境。

如需保護安裝和使用數位憑證的詳細資訊，請參閱撰寫安全安裝和[數位簽章](digital-signatures-and-windows-installer.md)[的指導方針](guidelines-for-authoring-secure-installations.md)，以及 Windows Installer 以及[從網際網路下載安裝](downloading-an-installation-from-the-internet.md)。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="remarks"></a>備註

如果有安裝或啟動這些程式的 Windows Installer 套件，則設定此原則也可讓非系統管理員的使用者以 LocalSystem 許可權執行任意程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[來源復原](source-resiliency.md)
</dt> <dt>

[AllowLockdownBrowse](allowlockdownbrowse.md)
</dt> </dl>

 

 




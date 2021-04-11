---
description: 將此每部電腦系統原則的值設定為 &\# 0034; 1&\# 0034; 可讓非系統管理員的使用者使用 [流覽] 對話方塊來找出受管理應用程式的來源。
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848981"
---
# <a name="allowlockdownbrowse"></a>AllowLockdownBrowse

將每部電腦 [系統原則](system-policy.md) 的值設定為 "1"，可讓非系統管理員的使用者使用 [[流覽] 對話方塊](browse-dialog.md) 來找出 [*受管理應用程式*](m-gly.md)的來源。 來源可能包含媒體，例如 CD-ROM、Url 和網路位置。 如需詳細資訊，請參閱 [來源復原](source-resiliency.md)。 Windows Installer 的預設值是，非受控使用者無法流覽受管理應用程式的新來源。 唯一可用的來源是已在產品的來源清單中註冊的來源。 如果設定此原則，非系統管理員的使用者可能會流覽已指派或已發佈應用程式的新來源，或針對所有使用者安裝的應用程式。 設定 AllowLockdownBrowse 也可讓非系統管理員的使用者在提高許可權的安裝期間，以 LocalSystem 許可權執行程式。

建議使用預設設定，以確保安全的環境。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="remarks"></a>備註

如果有安裝或啟動這些程式的 Windows Installer 套件，則設定此原則也可讓非系統管理員的使用者以 LocalSystem 許可權執行任意程式。

[DisableBrowse](disablebrowse.md) 會覆寫 AllowLockdownBrowse 並防止流覽，即使已設定 AllowLockdownBrowse 也是如此。

如需此原則與安裝來源互動的詳細資訊，請參閱 [管理安裝來源](managing-installation-sources.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[來源復原](source-resiliency.md)
</dt> <dt>

[AllowLockdownMedia](allowlockdownmedia.md)
</dt> </dl>

 

 




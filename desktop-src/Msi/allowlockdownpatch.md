---
description: 如果未設定每部電腦的系統原則，則只有系統管理員可以修補使用較高許可權安裝的現有產品。
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c827b23f8beecf02d3312358d7ece6b835619111428349850f4e597ce379cd53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145901"
---
# <a name="allowlockdownpatch"></a>AllowLockdownPatch

如果未設定每部電腦的 [系統原則](system-policy.md) ，則只有系統管理員可以修補使用較高許可權安裝的現有產品。 如果 AllowLockdownPatch 設為 "1"，非系統管理員的使用者在某些情況下，可以在使用較高的許可權執行安裝時，將修補程式套用至產品。 使用原則設定之後，修補程式就可以在使用較高的許可權執行安裝時安裝 [次要升級](minor-upgrades.md) ，修補程式無法安裝 [主要升級](major-upgrades.md)。 設定此原則也可讓非系統管理員的使用者在提高許可權的安裝期間，以 LocalSystem 許可權執行程式。

建議使用預設設定，以確保安全的環境。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **安裝程式**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="remarks"></a>備註

任何使用者都可以在 nonelevated 安裝期間套用修補程式。 將此每部電腦的 [系統原則](system-policy.md) 設定為 "1"，可讓非系統管理員的使用者在提高許可權的安裝期間，將修補程式套用至任何產品的額外彈性。 如果未設定此原則，非管理員使用者就無法將修補程式套用至已指派或已發佈的應用程式。

如果有安裝或啟動這些程式的 Windows Installer patch 套件，則設定此原則也可讓非系統管理員的使用者以 LocalSystem 許可權執行任意程式。

 

 




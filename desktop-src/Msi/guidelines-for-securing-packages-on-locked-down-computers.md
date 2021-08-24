---
description: 若要在鎖定的電腦上維護安全的軟體安裝，請在撰寫 Windows Installer 套件時遵守這些指導方針。
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: 保護鎖定電腦上的套件安全
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bcdb2770e165a8b0d99fbc2088ec4c3b113e5befa180a7d6d2598eee866a5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315298"
---
# <a name="securing-packages-on-locked-down-computers"></a>保護鎖定電腦上的套件安全

在撰寫將用於鎖定電腦的 Windows Installer 套件時遵循下列指導方針，有助於在安裝期間維護安全的環境：

-   測試套件是否與 Windows Installer 的電腦[系統原則](system-policy.md)相容。
-   請確定您已使用所有 [使用者介面層級](user-interface-levels.md)、無、基本、受限和完整封裝執行。
-   在 NTFS 磁碟分割上測試您的封裝，並以更 [*高*](e-gly.md) 和非提高許可權來進行。
-   從 Windows Installer 3.0 開始， [ (UAC) 修補的使用者帳戶控制](user-account-control--uac--patching.md)可讓非系統管理員使用者修補個別電腦內容中安裝的應用程式。 在 Windows Vista 和 Windows XP 上測試修補套件，以供具有系統管理員存取權的使用者和非系統管理員的使用者進行安裝。

 

 




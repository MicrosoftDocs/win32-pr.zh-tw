---
description: 如果此每部電腦系統原則的值設定為 &\# 0034; 2&\# 0034; 所有應用程式的安裝程式一律為停用。 如果此原則值設定為 &\# 0034; 1&\# 0034;，則會停用未受管理應用程式的安裝程式，但仍會針對受控應用程式啟用。
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846b8fb8c2c1127e59c82cce138a0956756d3447d6628cb61ef170a91e6290b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378556"
---
# <a name="disablemsi"></a>DisableMSI

如果每部電腦 [系統原則](system-policy.md) 的值設定為 "2"，則所有應用程式一律會停用安裝程式。 如果此原則值設定為 "1"，則會停用未受管理應用程式的安裝程式，但仍會針對受控應用程式啟用。

下表列出可能的設定。



| DisableMSI | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *預設值*  | 在 Windows Server 2003、Windows Server 2003 R2、Windows Server 2008 和 Windows Server 2008 R2 上，如果原則值為 Null、不存在，或1或2以外的任何數位，則會為受控應用程式啟用 Windows Installer。 系統會封鎖非受控應用程式安裝。<br/> 在 Windows XP、Windows Vista 和 Windows 7 上，會針對所有應用程式啟用 Windows Installer。 允許所有安裝作業。<br/> |
| 0          | Windows所有應用程式都已啟用安裝程式。 允許所有安裝作業。                                                                                                                                                                                                                                                                                                                                                      |
| 1          | 未受管理的應用程式會停用 Windows Installer，但仍會為受控應用程式啟用。 系統會封鎖非提高許可權的每個使用者安裝。 允許每位使用者的提高許可權，以及每部電腦的安裝。                                                                                                                                                                                                                        |
| 2          | Windows所有應用程式的安裝程式一律停用。 不允許安裝，包括修復、重新安裝或隨選安裝。                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **安裝程式**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





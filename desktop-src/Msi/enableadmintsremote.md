---
description: 從 Windows Server 2008 和 Windows Vista 開始，此原則不再具有任何作用。
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a644e6f0cb9200fd8a130a2cdb293e7658e3354b817f7378571fae0ab3b4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637102"
---
# <a name="enableadmintsremote"></a>EnableAdminTSRemote

從 Windows Server 2008 和 Windows Vista 開始，此原則不再具有任何作用。 系統管理員可以從終端機伺服器的主控台會話執行安裝。 系統管理員也可以從終端機伺服器的用戶端會話執行安裝。

如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 中的[終端機服務](/windows/desktop/TermServ/terminal-services-portal)。

* * 早于 Windows Server 2008 和 Windows Vista 的作業系統： * *

設定每一電腦的 [系統原則](system-policy.md) ，可讓系統管理員從終端機伺服器的用戶端會話執行安裝。 如果未設定此原則，系統管理員只能從主控台會話執行安裝。 非管理員的使用者永遠不能從用戶端會話執行安裝。 此原則的預設值僅允許系統管理員從主控台會話執行安裝。 系統管理員一律可以從終端機伺服器的用戶端會話，或從主控台會話進行系統 [管理安裝](administrative-installation.md) ，不論是否已設定此原則。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **安裝程式**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="remarks"></a>備註

如需詳細資訊，請參閱搭配[使用 Windows Installer 與終端機伺服器](using-windows-installer-with-a-terminal-server.md)。

 

 

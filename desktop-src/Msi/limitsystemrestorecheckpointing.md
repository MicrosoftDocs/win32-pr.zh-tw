---
description: 每一電腦的系統原則會依 Windows Installer 關閉檢查點的建立。
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989916"
---
# <a name="limitsystemrestorecheckpointing"></a>LimitSystemRestoreCheckpointing

每一電腦的 [系統原則](system-policy.md) 會依 Windows Installer 關閉檢查點的建立。

設定為0或不存在，安裝程式會進行安裝或卸載的一般檢查點檢查。 設定為1時，安裝程式不會建立檢查點。

此原則只會影響 Windows Installer 所設定的檢查點。 在 Windows XP 電腦上，系統管理員可能會決定停用 Windows Installer 內的檢查點，以改善效能。 [**系統還原**](../sr/system-restore-portal.md) 也會建立額外的檢查點。 如需詳細資訊，請參閱 [系統還原點和 Windows Installer](system-restore-points-and-the-windows-installer.md) ，以及 [設定自訂動作的還原點](setting-a-restore-point-from-a-custom-action.md)。

## <a name="registry-key"></a>登錄金鑰

在下列登錄機碼底下，設定名為 LimitSystemRestoreCheckpointing 的值。

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 原則 \\ Microsoft \\ Windows \\ Installer**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

 

 

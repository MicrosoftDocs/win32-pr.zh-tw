---
description: Windows Management Instrumentation (WMI) 具有新的登錄機碼，可啟用或停用 AutoRestore 存放庫功能。
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: 存放庫設定的登錄機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989934"
---
# <a name="registry-key-for-repository-configuration"></a>存放庫設定的登錄機碼

Windows Management Instrumentation (WMI) 具有新的登錄機碼，可啟用或停用 AutoRestore 存放庫功能。 如需還原 WMI 儲存機制的詳細資訊，請參閱 [備份或還原 wmi 存放庫](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11))。

在 Windows 7 中，預設行為是在偵測到存放庫損毀時，從備份的版本自動還原存放庫。 WMI 提供 **AutoRestoreEnabled** 登錄值以停用此功能。

WMI 的登錄機碼位於 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ 的登錄中。

<dl> <dt>

<span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**
</dt> <dd>

可讓使用者決定是否要使用 AutoRestore 存放庫功能。 依預設，此機碼設定為1，且已啟用 AutoRestore 存放庫功能。

可能的設定如下：

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Disabled

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

已啟用

</dd> </dl> </dd> </dl>

您可以使用群組原則管理主控台 (GPMC) 來修改 **AutoRestoreEnabled** 登錄值。 如需詳細資訊，請參閱 [群組原則管理主控台](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal)。

此程式提供有關如何啟用或停用 AutoRestore 儲存機制功能的詳細資料：

**使用群組原則來變更 **AutoRestoreEnabled** 索引鍵的預設值**

1.  開啟 GPMC。
2.   (GPO) 建立群組原則物件。
3.  編輯 GPO。
4.  流覽至 [喜好設定]/[Windows 設定]/[登錄]。
5.  以滑鼠右鍵按一下並選取 [新增]。 登錄。 此動作會顯示使用者介面，您可以在其中輸入登錄資訊。
6.  選取 [ **更新** ] 命令。
7.  選取下列登錄機碼路徑： **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ WBEM \\ CIMOM**。
8.  在 [ **名稱** ] 欄位中，輸入 **AutoRestoreEnabled**。
9.  在 [ **資料** ] 欄位中，輸入0以停用，或輸入1以啟用 AutoRestore 存放庫功能。
10. 按一下 [確定]。

 

 

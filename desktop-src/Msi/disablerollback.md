---
description: 如果此系統原則設定為1，安裝程式就不會在安裝期間儲存復原檔案，並停用安裝復原。
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943577"
---
# <a name="disablerollback"></a>DisableRollback

如果此 [系統原則](system-policy.md) 設定為1，安裝程式就不會在安裝期間儲存復原檔案，並停用安裝復原。 預設會啟用復原。 除非系統管理員絕對必要，否則建議不要使用此原則。 如需詳細資訊，請參閱 [復原安裝](rollback-installation.md)。

## <a name="registry-key"></a>登錄金鑰

若要針對個別使用者安裝停用復原，請在下列登錄機碼底下將 **DisableRollback** 設定為1：

**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

若要針對每部電腦安裝停用復原，請在下列登錄機碼底下將 **DisableRollback** 設定為1。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

 

 




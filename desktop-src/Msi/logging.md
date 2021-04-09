---
description: 只有當 &0034 未啟用記錄 \# ;/l&\# 0034; 命令列選項或 MsiEnableLog 時，才會使用每部電腦的系統原則。
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: '記錄 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693051"
---
# <a name="logging-windows-installer"></a>記錄 (Windows Installer) 

只有當 "/L" 命令列選項或 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)未啟用記錄功能時，才會使用每部電腦的 [系統原則](system-policy.md)。 如果在此情況下設定此原則，安裝程式會在% temp% 中建立具有隨機名稱： MSI 的記錄檔 \* 。日誌。 將原則值設定為字元字串，以指定記錄模式。 使用相同的字元，指定 "/L" [命令列選項](command-line-options.md)所使用的記錄模式原則。 請注意，您不能針對原則使用 "+" 和 " \* "。

您可以使用原則、命令列選項或以程式設計方式來設定記錄模式。 如需可用於設定記錄模式之所有方法的詳細資訊，請參閱[Windows Installer 記錄](windows-installer-logging.md)] 區段中的[一般記錄](normal-logging.md)。

您可以防止將機密資訊（例如密碼）輸入記錄檔中，並使其成為可見。 如需詳細資訊，請參閱[防止機密資訊寫入記錄](preventing-confidential-information-from-being-written-into-the-log-file.md)檔

## <a name="registry-key"></a>登錄金鑰

在下列登錄機碼底下，設定名為 [記錄] 的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>資料類型

**REG \_ SZ**

 

 




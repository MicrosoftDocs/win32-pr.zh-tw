---
description: 您可以從命令列或從程式完全或部分地重新安裝應用程式，以將小型更新套用至應用程式。
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: 重新安裝產品以套用小型更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944028"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a>重新安裝產品以套用小型更新

您可以從命令列或從程式完全或部分地重新安裝應用程式，以將小型更新套用至應用程式。

**若要將 small update 傳播給目前的使用者 (這是從命令列完整重新安裝)**

1.  從命令列使用： **msiexec \[ /fvomus** _path 將 .msi_ 檔案 *_\]_* 或 **msiexec/i \[** 路徑更新 _為已更新的 .msi 檔案。_ *_\] 重新安裝 = ALL REINSTALLMODE = vomus reinstall_*。
2.  更新的 .msi 檔案會快取在使用者的電腦上。 請注意，使用者無法使用 [新增/移除程式] 重新安裝產品，因為更新的 .msi 檔案尚未在使用者的電腦上。

**若要將小型更新傳播給目前的使用者 (這是從程式完整重新安裝)**

1.  從程式中，呼叫 [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) 並指定 REINSTALLMODE \_ PACKAGE、REINSTALLMODE \_ FILEOLDERVERSION、REINSTALLMODE \_ MACHINEDATA、REINSTALLMODE \_ USERDATA 和 REINSTALLMODE \_ 快速鍵
2.  更新的 .msi 檔案會快取在使用者的電腦上。

下列方法會啟動僅重新安裝受 small update 影響的功能或元件。

**若要將小型更新傳播給目前的使用者 (這是部分重新安裝)**

1.  取得受 small update 影響的功能和元件名稱清單。
2.  從命令提示字元使用： **msiexec/i \[** _path to updated .msi file_ *_\] 重新安裝 = \[_* _Feature list \]_ **REINSTALLMODE = vomus reinstall**。
3.  更新的 .msi 檔案會快取在使用者的電腦上。

 

 




---
title: '登錄專案 (COM) '
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 深入瞭解： (COM) 的登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111453"
---
# <a name="registry-entries-com"></a>登錄專案 (COM) 

下列登錄機碼中的登錄值會控制 COM 功能的各個層面：

-   [**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別**](hkey-local-machine-software-classes.md)
-   [**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Ole**](hkey-local-machine-software-microsoft-ole.md)
-   [**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion**](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

從 Windows Server 2003，COM 只會使用目前的進程權杖來決定要存取的登錄區，而不是執行緒 token。 如果 COM 無法存取使用者設定檔登錄區，它將會存取 **HKEY \_ 本機 \_ 電腦 \\ 系統** hive。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[登錄](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 

---
title: 虛擬通道用戶端註冊
description: 您必須將用戶端 DLL 的名稱儲存在登錄中。
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682506"
---
# <a name="virtual-channel-client-registration"></a>虛擬通道用戶端註冊

您必須將用戶端 DLL 的名稱儲存在登錄中。

在登錄中，將子機碼新增至下列其中一個位置：

**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **終端機伺服器用戶端** \\ **預設** 的 \\ **載入** 宏

**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **終端機伺服器用戶端** \\ **連接** \\ **載入** 宏

> [!Note]  
> 在登錄路徑中， *連接* 代表連線管理員中的連接名稱。

 

**\\ 預設的 \\ 載入** 鍵底下的專案會套用至所有連接。 **\\ ***Connection*** \\ Addins** 索引鍵底下的專案只適用于 *連接* 所識別的連接。 您可以使用連線管理員來建立和管理連接。

您可以為子機碼指定任何名稱。 它必須包含 **reg \_ Sz** 或 **reg \_ EXPAND \_ sz** 值，而且可以選擇性地包含 **reg \_ DWORD** 值。 **Reg \_ Sz** 或 **reg \_ 展開 \_ SZ** 值的語法如下所示。

``` syntax
Name = DLLname
```

如果 **Name** 是 **REG \_ EXPAND \_ SZ** 值，它可以包含展開于執行時間的未展開環境變數。

*DLLname* 的值可以是完整路徑。 如果 *DLLname* 不包含路徑，則會使用標準 DLL 搜尋策略。 如需詳細資訊，請參閱 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)的備註一節。

 

 
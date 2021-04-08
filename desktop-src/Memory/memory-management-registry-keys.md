---
description: 32位系統上的系統虛擬位址 (VA) 空間，可能會因為片段而用盡。 您可以使用數個登錄機碼，在遇到此問題的32位系統上設定記憶體限制。
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: 記憶體管理登錄機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852948"
---
# <a name="memory-management-registry-keys"></a>記憶體管理登錄機碼

32位系統上的系統虛擬位址 (VA) 空間，可能會因為片段而用盡。 您可以使用數個登錄機碼，在遇到此問題的32位系統上設定記憶體限制。 64位系統上的系統 VA 空間不受片段的耗盡，因此，這些金鑰組64位系統沒有任何影響。

若為32位系統，您必須在下列登錄機碼底下明確建立這些記憶體管理登錄機碼：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **目前的控制集** \\ **控制** \\ **會話管理員** \\ **記憶體管理**

**Windows Server 2008 和 Windows Vista：** 從 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 開始，這些登錄機碼可在32位系統上使用。

若為32位和64位系統上的預設記憶體和位址空間限制，請參閱 [Windows 版本的記憶體限制](memory-limits-for-windows-releases.md)。

下表描述可用來在32位系統上設定記憶體限制的記憶體管理登錄機碼。 所有這些索引鍵都具有 REG \_ DWORD 類型，以及範圍從0到 2048 MB 的可能值。 預設值為0，表示不會強制執行任何限制。 值會自動四捨五入至下一個系統 VA 配置界限，也就是32位系統上的 2 MB，其 [實體位址延伸](physical-address-extension.md) (pae) 啟用，而32位系統上的 4 mb 未啟用 pae。



| Key                   | 描述                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NonPagedPoolLimit** | 指定可供非分頁集區使用的系統 VA 空間數量上限。 在某些情況下，這項限制可能會超過一小部分。 |
| **PagedPoolLimit**    | 指定可供分頁集區使用的系統 VA 空間數量上限。                                                                            |
| **SessionSpaceLimit** | 指定會話空間配置可以使用的系統 VA 空間數量上限。                                                                 |
| **SystemCacheLimit**  | 指定系統快取可使用的系統 VA 空間數量上限。 在某些情況下，這項限制可能會超過一小部分。  |
| **SystemPtesLimit**   | 指定使用系統分頁表專案 (Pte) 的 i/o 對應和其他資源可以使用的最大系統 VA 空間量。            |



 

判斷系統 VA 空間是否已用盡，需要使用內核偵錯工具。 如需詳細資訊，請參閱＜ [Windows 偵錯工具](https://msdn.microsoft.com/library/cc267445.aspx)＞。

 

 




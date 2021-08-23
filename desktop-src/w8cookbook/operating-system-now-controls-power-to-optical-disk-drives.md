---
title: 作業系統現在可控制磁片磁碟機的電源
description: 作業系統現在可控制磁片磁碟機的電源
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc43ad47f6a9468c2850627f267d433bfa346d059231d5daa91e860d5a793aef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593798"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a>作業系統現在可控制磁片磁碟機的電源

## <a name="platforms"></a>平台

**用戶端**– Windows 8  
**伺服器**– Windows Server 2012  


## <a name="description"></a>描述

在舊版 Windows 中，光碟機的電源不會在光碟機未使用時受到管理。 現在，如果光學磁片磁碟機中沒有媒體 (奇怪的) ，作業系統會關閉光碟機的電源。 這項功能稱為零的強大 (ZPODD) 。 這項功能僅適用于使用超薄 SATA (串列先進技術附件) 連接器的光碟機。

## <a name="manifestation"></a>表現

我們找不到這種新行為的負面影響;不過，您應該要注意，因為它可能會導致媒體寫入軟體發生非預期的行為。

## <a name="mitigation"></a>降低

若要還原為 alwayson 狀態，請關閉登錄中的這項功能。 登錄值的絕對路徑為：

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

其類型為 DWORD (32 位) ，如果其值為0，則 ZPODD 會停用;如果是任何其他值，則會啟用 ZPODD。

## <a name="tests"></a>測試

測試您的媒體撰寫軟體是否有因這項新功能而發生的任何異常狀況。 請 [通知 Microsoft](mailto:OptIssue@microsoft.com) 您使用這項新功能時所發現的任何問題。

 

 





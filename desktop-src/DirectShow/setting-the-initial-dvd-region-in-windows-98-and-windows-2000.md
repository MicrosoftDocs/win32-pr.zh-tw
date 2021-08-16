---
description: 設定初始 DVD 區域
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: 設定初始 DVD 區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bf019c7d5ddae8efb257435e1b23037575a37f809ef012190b49c619cc3211
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102318"
---
# <a name="setting-the-initial-dvd-region"></a>設定初始 DVD 區域

系統製造商必須在電腦上選取 DVD 光碟機的初始 DVD 區域。

> [!Note]  
> 只有加密的光碟可以用來設定區域。

 

### <a name="windows-2000-and-later"></a>Windows 2000 和更新版本

從 Windows 2000 開始，預設的 DVD 區域會根據設定電腦的地區設定來選取。 如果磁片磁碟機中有光碟片，Windows 2000 一律會使用此預設區域以及光碟區域來設定 DVD 光碟機的初始區域。 系統製造商不需要執行任何動作來設定 Windows 2000 或更新版本 DVD 光碟機的初始區域。

針對 RPC1 磁片磁碟機，如果開機時磁片磁碟機中沒有光碟片，則預設區域只會根據電腦的地區設定來設定。 在開機時，如果磁片磁碟機中有 DVD 光碟，則會選取預設區域作為磁片磁碟機的區域，前提是它符合光碟的區域;否則，光碟上的最社區域會挑選為磁片磁碟機的初始區域。 如果預設值不正確，使用者 (或系統製造商) 會允許一項剩餘的變更。

針對 RPC2 磁片磁碟機，如果在安裝程式期間 Windows 2000 發現磁片磁碟機沒有設定任何區域，則會嘗試挑選上面的區域，但只有在磁片磁碟機中有光碟時。  (RPC1 磁片磁碟機會選擇沒有任何磁片磁碟機) 的區域。 設定 RPC2 磁片磁碟機的區域之後，重新安裝或全新的作業系統安裝並不會自動變更。

OEM 可以設定包含系統預設 DVD 區域的登錄機碼。 第一次開機時，磁片磁碟機區域會設定為此值。 Windows 2000 和更新版本上的登錄機碼為 HKLM \\ System \\ CurrentControlSet \\ Control \\ Class \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion (binary) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 中的 DVD 區域變更支援](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 




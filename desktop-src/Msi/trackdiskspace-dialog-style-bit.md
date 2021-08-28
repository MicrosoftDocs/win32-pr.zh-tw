---
description: 如果設定此位，對話方塊會定期呼叫安裝程式。
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: TrackDiskSpace 對話方塊樣式位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8e12a77f0b7e67bd82e094953a2bacd8204d93b444dc6bd1dc378602e67809
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810568"
---
# <a name="trackdiskspace-dialog-style-bit"></a>TrackDiskSpace 對話方塊樣式位

如果設定此位，對話方塊會定期呼叫安裝程式。 如果屬性變更，則會通知對話方塊上的控制項。 如果對話方塊上有控制項指出磁碟空間，則可以使用這個樣式。 如果使用者切換到另一個應用程式、新增或移除檔案，或修改可用的磁碟空間，您可以使用此樣式快速執行變更。

任何依賴 [**OutOfDiskSpace**](outofdiskspace.md) 屬性來判斷是否要顯示對話方塊的對話方塊都必須設定對話方塊的 TrackDiskSpace 對話方塊樣式位，以動態更新目標磁片區上的空間。

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                                |
|---------|-------------|-----------------------------------------|
| 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace** |



 

 

 




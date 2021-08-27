---
description: PROMPTROLLBACKCOST 屬性會指定如果已啟用復原安裝功能，且沒有足夠的磁碟空間來完成安裝，則安裝程式所採取的動作。PROMPTROLLBACKCOST 可能的值如下所示。ValueActionPDisplay 對話方塊，詢問是否要在沒有回復的情況下繼續進行。DDisable 復原並繼續，而不要求使用者。FFail 與磁碟空間不足的錯誤提示。
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: PROMPTROLLBACKCOST 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71cca3134593039354735e2e306a924620db8100eb0fd0e0a51f392c58f61897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129038"
---
# <a name="promptrollbackcost-property"></a>PROMPTROLLBACKCOST 屬性

**PROMPTROLLBACKCOST** 屬性會指定如果已啟用 [復原安裝](rollback-installation.md)功能，且沒有足夠的磁碟空間來完成安裝，則安裝程式所採取的動作。

**PROMPTROLLBACKCOST** 可能的值如下所示。



| 值 | 動作                                                              |
|-------|---------------------------------------------------------------------|
| P     | 顯示對話方塊，詢問是否要在沒有回復的情況下繼續進行。 |
| D     | 停用復原並繼續，而不要求使用者。                  |
| F     | 發生磁碟空間不足的錯誤提示時失敗。                       |



 

## <a name="remarks"></a>備註

當使用者介面是在基本或無 UI 層級執行時，安裝程式會自動處理所有的磁碟空間邏輯。

當使用者介面在完整層級執行時，可以提供其他選項（例如，在繼續進行復原之前提示）、停用復原，或在磁片已滿時繼續進行而不回復。 封裝開發人員可自行撰寫對話方塊順序，為使用者提供適當的選擇。 可用來進行這項作業的元素有 [EnableRollback ControlEvent](enablerollback-controlevent.md)、 [**OutOfDiskSpace**](outofdiskspace.md) property、 [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) 屬性和 **PROMPTROLLBACKCOST** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 





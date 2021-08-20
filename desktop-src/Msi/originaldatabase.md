---
description: Windows Installer 將 OriginalDatabase 屬性設定為用來啟動安裝的安裝資料庫路徑。
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: OriginalDatabase 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b8ec6b77d013ee89d081c0ff20e3ad00750454e1fa9299d364fdb94e69ccb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145531"
---
# <a name="originaldatabase-property"></a>OriginalDatabase 屬性

Windows Installer 將 **OriginalDatabase** 屬性設定為用來啟動安裝的安裝資料庫路徑。 如果是從命令列啟動安裝，則此值取決於 [**REINSTALLMODE**](reinstallmode.md) 屬性中是否有 (-v 旗標) 的重新緩存套件選項。



| 安裝方式                                                                                                                                                                                  | OriginalDatabase 值                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 藉由叫用安裝套件的路徑來啟動任何安裝 (.msi 檔案) 。                                                                                                              | 安裝套件的路徑 (.msi 檔案) 。 |
| 從命令列啟動安裝。 安裝不是從封裝路徑啟動。 [**REINSTALLMODE**](reinstallmode.md)屬性中有 (-v 旗標) 的重新緩存選項。     | 來源上資料庫的路徑。           |
| 從命令列啟動安裝。 安裝不是從封裝路徑啟動。 [**REINSTALLMODE**](reinstallmode.md)屬性中沒有重新緩存選項 (-v 旗標) 。 | 快取資料庫的路徑。                  |



 

## <a name="remarks"></a>備註

在第一次安裝時， [ResolveSource 動作](resolvesource-action.md) 之前排序的自訂動作可以使用 **OriginalDatabase** 屬性來判斷安裝來源的位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 





---
description: Windows Installer 將 OriginalDatabase 屬性設定為用來啟動安裝的安裝資料庫路徑。
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: OriginalDatabase 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976065"
---
# <a name="originaldatabase-property"></a>OriginalDatabase 屬性

Windows Installer 將 **OriginalDatabase** 屬性設定為用來啟動安裝的安裝資料庫路徑。 如果是從命令列啟動安裝，則此值取決於 [**REINSTALLMODE**](reinstallmode.md) 屬性中是否有 (-v 旗標) 的重新緩存套件選項。



| 安裝方式                                                                                                                                                                                  | OriginalDatabase 值                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 藉由叫用安裝套件的路徑來啟動的任何安裝 ( .msi 檔案) 。                                                                                                              | 安裝套件的路徑 ( .msi 檔案) 。 |
| 從命令列啟動安裝。 安裝不是從封裝路徑啟動。 [**REINSTALLMODE**](reinstallmode.md)屬性中有 (-v 旗標) 的重新緩存選項。     | 來源上資料庫的路徑。           |
| 從命令列啟動安裝。 安裝不是從封裝路徑啟動。 [**REINSTALLMODE**](reinstallmode.md)屬性中沒有重新緩存選項 (-v 旗標) 。 | 快取資料庫的路徑。                  |



 

## <a name="remarks"></a>備註

在第一次安裝時， [ResolveSource 動作](resolvesource-action.md) 之前排序的自訂動作可以使用 **OriginalDatabase** 屬性來判斷安裝來源的位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 





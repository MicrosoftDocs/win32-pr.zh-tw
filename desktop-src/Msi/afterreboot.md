---
description: 當 ForceReboot 動作叫用重新開機之後，安裝程式會將 AFTERREBOOT 屬性設定為1。 安裝程式會在重新開機之後，將 AFTERREBOOT = 1 新增至命令列執行。
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: AFTERREBOOT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf8fb80a3d8ff167f93aab6c95fc3eadb8b5312daf9d2a2856f01cb7d01ee383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145911"
---
# <a name="afterreboot-property"></a>AFTERREBOOT 屬性

當 [ForceReboot 動作](forcereboot-action.md)叫用重新開機之後，安裝程式會將 **AFTERREBOOT** 屬性設定為1。 安裝程式會在重新開機之後，將 AFTERREBOOT = 1 新增至命令列執行。

## <a name="remarks"></a>備註

[ForceReboot 動作](forcereboot-action.md)必須一律搭配條件陳述式使用，讓安裝程式只在必要時才觸發重新開機。 如果已取代特定檔案或已安裝特定元件，則可能需要重新開機。 每項產品都有不同的案例，而且可能需要自訂動作來判斷是否需要重新開機。 ForceReboot 動作的條件通常會使用 **AFTERREBOOT** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[系統重新開機](system-reboots.md)
</dt> </dl>

 

 





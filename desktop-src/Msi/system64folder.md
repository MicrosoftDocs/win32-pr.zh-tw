---
description: 安裝程式會將 System64Folder 屬性設定為預先定義之 System64 資料夾的完整路徑。 現有的 System64Folder 屬性會設定為對應的32位資料夾。
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: System64Folder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995966"
---
# <a name="system64folder-property"></a>System64Folder 屬性

安裝程式會將 **System64Folder** 屬性設定為預先定義之 System64 資料夾的完整路徑。 現有的 **System64Folder** 屬性會設定為對應的32位資料夾。

## <a name="remarks"></a>備註

安裝程式會在64位 Windows 上設定這個屬性。 例如，在64位的 Windows 上，此值可能是 C： \\ Window \\ System32。 這個屬性不會用於32位的 Windows 上。

此資料夾通常是 Windows 資料夾的子目錄。 不過，它會在設定共用視窗時位於伺服器上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 





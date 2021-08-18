---
description: 安裝程式會將 TempFolder 屬性設定為 Temp 資料夾的完整路徑。作者應該不需要設定 TempFolder 屬性。
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: TempFolder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5ded141982c12204eb5267357cedded6521eccb7cc47a3bf000b026faf9aed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626501"
---
# <a name="tempfolder-property"></a>TempFolder 屬性

安裝程式會將 **TempFolder** 屬性設定為 Temp 資料夾的完整路徑。

作者應該不需要設定 **TempFolder** 屬性。 Windows安裝程式會使用 [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha)函式來抓取為暫存檔案指定的目錄路徑，並設定這個屬性。

## <a name="remarks"></a>備註

這個屬性的通用值為 C： \\ Temp。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 

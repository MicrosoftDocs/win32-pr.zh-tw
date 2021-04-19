---
description: 安裝程式會將 TempFolder 屬性設定為 Temp 資料夾的完整路徑。作者應該不需要設定 TempFolder 屬性。
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: TempFolder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999106"
---
# <a name="tempfolder-property"></a>TempFolder 屬性

安裝程式會將 **TempFolder** 屬性設定為 Temp 資料夾的完整路徑。

作者應該不需要設定 **TempFolder** 屬性。 Windows Installer 使用 [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) 函式來取出為暫存檔案指定的目錄路徑，並設定這個屬性。

## <a name="remarks"></a>備註

這個屬性的通用值為 C： \\ Temp。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 

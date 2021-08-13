---
description: ROOTDRIVE 屬性會指定安裝目的地目錄的預設磁片磁碟機。
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: ROOTDRIVE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ca4a3230dde5086b1383f3016da30d99976cf6560d0be994ecb0aaccc0ba6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625735"
---
# <a name="rootdrive-property"></a>ROOTDRIVE 屬性

**ROOTDRIVE** 屬性會指定安裝目的地目錄的預設磁片磁碟機。 如果 [目錄資料表](directory-table.md) 的目錄資料行以未定義的屬性名稱來指出根目的地目錄，安裝程式就會使用 **ROOTDRIVE** 屬性的值來解析目的地目錄的路徑。

如果未在命令列上設定 **ROOTDRIVE** ，或在 [屬性工作表](property-table.md)中撰寫，則安裝程式會設定這個屬性。 在 [系統管理安裝](administrative-installation.md) 期間，安裝程式會將 **ROOTDRIVE** 設定為第一個可寫入的連線網路磁碟機機。 如果它不是系統管理安裝，或是安裝程式找不到任何網路磁碟機機，則安裝程式會將 **ROOTDRIVE** 設定為可寫入至具有最多可用空間的本機磁片磁碟機。

這個屬性的值必須以 ' ' 結尾 \\ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 





---
description: PRIMARYFOLDER 是全域屬性，可讓作者指定主要資料夾以進行安裝。
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: PRIMARYFOLDER 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2fce0875a9b3fb63dfc0dccb1a351e35577ff61ebcb4a59a25c10468d1684
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381268"
---
# <a name="primaryfolder-property"></a>PRIMARYFOLDER 屬性

**PRIMARYFOLDER** 是全域屬性，可讓作者指定主要資料夾以進行安裝。 這個屬性的值必須是存在於 [目錄資料表](directory-table.md)中之目錄的索引鍵名稱。

安裝程式會在設定 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性、 [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) 屬性、 [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) 屬性和 [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) 屬性的值時，使用主要資料夾的解析路徑來決定要使用的磁片區。 安裝程式會將這些後面的屬性值提供給使用者介面中的使用者，以協助他們管理磁碟空間。 通常封裝作者可以選取最大的資料夾做為主要資料夾。

這個屬性的值必須是 [目錄資料表](directory-table.md)中所找到目錄記錄的索引鍵名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 





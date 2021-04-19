---
description: PRIMARYFOLDER 是全域屬性，可讓作者指定主要資料夾以進行安裝。
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: PRIMARYFOLDER 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987037"
---
# <a name="primaryfolder-property"></a>PRIMARYFOLDER 屬性

**PRIMARYFOLDER** 是全域屬性，可讓作者指定主要資料夾以進行安裝。 這個屬性的值必須是存在於 [目錄資料表](directory-table.md)中之目錄的索引鍵名稱。

安裝程式會在設定 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性、 [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) 屬性、 [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) 屬性和 [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) 屬性的值時，使用主要資料夾的解析路徑來決定要使用的磁片區。 安裝程式會將這些後面的屬性值提供給使用者介面中的使用者，以協助他們管理磁碟空間。 通常封裝作者可以選取最大的資料夾做為主要資料夾。

這個屬性的值必須是 [目錄資料表](directory-table.md)中所找到目錄記錄的索引鍵名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 





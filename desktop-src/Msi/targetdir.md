---
description: TARGETDIR 屬性會指定安裝的根目的地目錄。
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: TARGETDIR 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990689"
---
# <a name="targetdir-property"></a>TARGETDIR 屬性

**TARGETDIR** 屬性會指定安裝的根目的地目錄。 **TARGETDIR** 必須是 [目錄](directory-table.md) 資料表中一個根目錄的名稱。 可能只有一個根目的地目錄。 在 [系統管理安裝](administrative-installation.md) 期間，此屬性會指定要複製安裝套件的位置。 在非系統管理安裝期間，此屬性會指定根目的地目錄。

若要指定根目的地目錄，請將目錄資料表的 [目錄] 資料行設定為 [ **TARGETDIR** ] 屬性，並將 [DefaultDir] 資料行設定為 [ [**SourceDir**](sourcedir.md) ] 屬性。 如果定義了 **TARGETDIR** 屬性，則會將目的地目錄解析為屬性的值。 如果未定義 **TARGETDIR** 屬性，則會使用 [**ROOTDRIVE**](rootdrive.md) 屬性來解析路徑。 如需使用 **TARGETDIR** 屬性的詳細資訊，請參閱 [使用目錄資料表](using-the-directory-table.md)。

請注意， **TARGETDIR** 屬性的值通常是在命令列或透過使用者介面設定。 由於本機磁片磁碟機的設定不同，因此不建議在 [屬性工作表](property-table.md)中撰寫路徑來設定 **TARGETDIR** 。

如需如何在安裝期間變更 TARGETDIR 的詳細資訊，請參閱 [變更目錄的目標位置。](changing-the-target-location-for-a-directory.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 





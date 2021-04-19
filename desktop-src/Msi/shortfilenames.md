---
description: 設定 SHORTFILENAMES 屬性會導致將短檔案名用於目標檔案的名稱，而不是完整的檔案名。 它不會影響安裝程式在來源尋找的檔案名。
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: SHORTFILENAMES 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980239"
---
# <a name="shortfilenames-property"></a>SHORTFILENAMES 屬性

設定 **SHORTFILENAMES** 屬性會導致將短檔案名用於目標檔案的名稱，而不是完整的檔案名。 它不會影響安裝程式在來源尋找的檔案名。

## <a name="default-value"></a>預設值

如果未設定 **SHORTFILENAMES** 屬性，而且目標磁片區支援長名稱，則安裝程式會使用完整名稱。 如果目標磁片區不支援長名稱，則安裝程式會使用簡短名稱。

## <a name="remarks"></a>備註

當設定 **SHORTFILENAMES** 屬性時，安裝程式會使用檔案 \| [資料表](file-table.md) 或 [目錄資料表](directory-table.md)中所列之任何短組的簡短檔案名，建立資料夾並安裝檔案。

應用程式可以使用 [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) 函式來取出指定檔案路徑的簡短路徑形式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 

---
description: 安裝程式物件的 Get-filehash 方法會取得檔案的路徑，並傳回該檔案的128位雜湊。 檔案雜湊資訊會以記錄物件的形式傳回。 整個128位檔案雜湊會傳回為 4 32 位 IntegerData 屬性欄位。
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Get-filehash 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986804"
---
# <a name="installerfilehash-method"></a>Get-filehash 方法

[**安裝程式物件**](installer-object.md)的 **get-filehash** 方法會取得檔案的路徑，並傳回該檔案的128位雜湊。 檔案雜湊資訊會以 [**記錄物件**](record-object.md)的形式傳回。 整個128位檔案雜湊會傳回為 4 32 位 [**IntegerData**](record-integerdata.md) 屬性欄位。

在 [**記錄物件**](record-object.md)中傳回的值會對應至 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)所傳回之 [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo)結構的四個欄位。 四個欄位的編號在 [MsiFileHash 資料表](msifilehash-table.md)中是以1為基礎。

-   欄位1對應至 HashPart1 資料行。
-   欄位2對應于 HashPart2 資料行。
-   欄位3對應于 HashPart3 資料行。
-   欄位4對應于 HashPart4 資料行。

## <a name="syntax"></a>語法


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*FilePath* 
</dt> <dd>

要雜湊處理之檔案的路徑。

</dd> <dt>

*選項* 
</dt> <dd>

保留供未來使用。

此參數的值必須是 0 (零) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，這個方法會傳回包含檔案雜湊的 [**記錄物件**](record-object.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預設檔案版本控制](default-file-versioning.md)
</dt> <dt>

[管理檔案大小和版本](manage-file-sizes-and-versions.md)
</dt> <dt>

[MsiFileHash 資料表](msifilehash-table.md)
</dt> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 





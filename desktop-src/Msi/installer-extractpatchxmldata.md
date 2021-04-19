---
description: 安裝程式物件的 ExtractPatchXMLData 方法會將修補程式的資訊以 XML 字串的形式解壓縮。 此資訊可以用來判斷修補程式是否適用于目標系統。 這個方法會呼叫 MsiExtractPatchXMLData。
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: ExtractPatchXMLData 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985962"
---
# <a name="installerextractpatchxmldata-method"></a>ExtractPatchXMLData 方法

[**安裝程式**](installer-object.md)物件的 **ExtractPatchXMLData** 方法會將修補程式的資訊以 XML 字串的形式解壓縮。 此資訊可以用來判斷修補程式是否適用于目標系統。 這個方法會呼叫 [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)。

## <a name="syntax"></a>語法


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*PatchPath* 
</dt> <dd>

要從中解壓縮適用性資訊之修補程式的完整路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





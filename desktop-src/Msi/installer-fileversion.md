---
description: 安裝程式物件的 FileVersion 方法會使用安裝程式預期在資料庫中找到它們的格式，傳回路徑中指定之路徑的版本字串或語言字串。
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: FileVersion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982505"
---
# <a name="installerfileversion-method"></a>FileVersion 方法

[**安裝程式**](installer-object.md)物件的 **FileVersion** 方法會使用安裝程式預期在資料庫中找到它們的格式，*傳回路徑中* 指定之路徑的版本字串或語言字串。 針對版本，這是 " \# ... \# \# \# " 格式的字串。 針對語言，這是十進位語言識別項。

## <a name="syntax"></a>語法


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* 
</dt> <dd>

必要的字串，其中包含檔案的路徑。

</dd> <dt>

*Language* 
</dt> <dd>

旗標，用於指定傳回的值是否為語言識別項或版本字串。 TRUE 會傳回語言，FALSE 會傳回版本。 這個參數是選擇性的，預設值是 FALSE。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





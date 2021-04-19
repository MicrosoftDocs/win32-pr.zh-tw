---
description: 安裝程式物件的 FileAttributes 屬性會傳回數位，表示檔案或資料夾之指定路徑的合併檔案屬性。
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: 'FileAttributes 屬性 (Windows. .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988258"
---
# <a name="installerfileattributes-property"></a>FileAttributes 屬性

[**安裝程式**](installer-object.md)物件的 **FileAttributes** 屬性會傳回數位，表示檔案或資料夾之指定路徑的合併檔案屬性。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a>屬性值

檔案或資料夾的必要路徑。 部分路徑會假設目前的目錄。

## <a name="remarks"></a>備註

**FileAttributes** 屬性會傳回下列值。



| 檔案屬性              | 值      | 值 |
|-----------------------------|------------|-------|
| FILE\_ATTRIBUTE\_READONLY   | 0x00000001 | 1     |
| FILE\_ATTRIBUTE\_HIDDEN     | 0x00000002 | 2     |
| FILE\_ATTRIBUTE\_SYSTEM     | 0x00000004 | 4     |
| FILE\_ATTRIBUTE\_DIRECTORY  | 0x00000010 | 16    |
| 檔 \_ 屬性 \_ 暫存  | 0x00000100 | 256   |
| FILE\_ATTRIBUTE\_COMPRESSED | 0x00000800 | 2048  |
| FILE\_ATTRIBUTE\_OFFLINE    | 0x00001000 | 4096  |



 

如果檔案或資料夾不存在或無法存取，則會傳回–1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| 標頭<br/>  | <dl> <dt>：。H</dt> </dl>                                                                                                                                                            |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





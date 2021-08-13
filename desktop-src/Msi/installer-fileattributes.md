---
description: 安裝程式物件的 FileAttributes 屬性會傳回數位，表示檔案或資料夾之指定路徑的合併檔案屬性。
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: 'FileAttributes 屬性 (Windows. h) '
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
ms.openlocfilehash: 7fe43028d856ca26b1c5e8fa21a88a3b77381670ccc044a79f10d3b922f38c21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630911"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| 標頭<br/>  | <dl> <dt>Windows。h</dt> </dl>                                                                                                                                                            |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





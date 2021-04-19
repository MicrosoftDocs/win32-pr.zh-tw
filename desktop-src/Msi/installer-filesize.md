---
description: 安裝程式物件的 FileSize 方法會使用 WIN32 API 呼叫來傳回 Path 中指定之檔案的大小。
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: FileSize 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 593319b88e3942ae6caa1399adbe2e596bf6e737
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986590"
---
# <a name="installerfilesize-method"></a>FileSize 方法

[**安裝程式**](installer-object.md)物件的 **FileSize** 方法會使用 WIN32 API 呼叫來傳回 *Path* 中指定之檔案的大小。

## <a name="syntax"></a>語法


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* 
</dt> <dd>

必要的字串，其中包含檔案的路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





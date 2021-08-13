---
description: 安裝程式物件的環境屬性是讀寫屬性，它是目前進程之環境變數的字串值。
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: 安裝程式. 環境屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f24237da6c140ef0d38ff17591bf214698cfa6731bd4e8d3cfcaa613b335404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631684"
---
# <a name="installerenvironment-property"></a>安裝程式. 環境屬性

[**安裝程式**](installer-object.md)物件的 **環境** 屬性是讀寫屬性，它是目前進程之環境變數的字串值。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a>屬性值

要讀取或寫入的環境變數名稱。 這不區分大小寫。

## <a name="remarks"></a>備註

使用 **環境** 屬性設定環境變數只會影響作用中的會話。 若要對環境變數進行持續變更，請使用 [環境資料表](environment-table.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





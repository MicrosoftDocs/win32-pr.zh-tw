---
description: Session 物件的 SourcePath 屬性是唯讀屬性，可提供來源媒體或伺服器映射上所指定資料夾的完整路徑。
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Session 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996489"
---
# <a name="sessionsourcepath-property"></a>Session 屬性

[**Session**](session-object.md)物件的 **SourcePath** 屬性是唯讀屬性，可提供來源媒體或伺服器映射上所指定資料夾的完整路徑。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a>屬性值

需要區分大小寫的資料夾屬性名稱，如 [目錄資料表](directory-table.md)的主鍵所指定。 如果資料夾不存在，就會產生錯誤。

## <a name="remarks"></a>備註

如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





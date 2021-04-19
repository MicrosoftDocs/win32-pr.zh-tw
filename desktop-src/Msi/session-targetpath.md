---
description: Session 物件的 TargetPath 屬性是讀寫屬性，可提供安裝目標磁片磁碟機上指定之資料夾的完整路徑。
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: TargetPath 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984871"
---
# <a name="sessiontargetpath-property"></a>TargetPath 屬性

[**Session**](session-object.md)物件的 **TargetPath** 屬性是讀寫屬性，可提供安裝目標磁片磁碟機上指定之資料夾的完整路徑。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a>屬性值

需要區分大小寫的資料夾屬性名稱，如 [目錄資料表](directory-table.md)的主鍵所指定。 如果資料夾不存在，就會產生錯誤。

## <a name="remarks"></a>備註

如果已為目前使用者或其他使用者安裝使用這些路徑的元件，請不要嘗試設定目標路徑。 檢查 [**ProductState**](productstate.md) 屬性，以判斷是否已安裝包含該元件的產品。

如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





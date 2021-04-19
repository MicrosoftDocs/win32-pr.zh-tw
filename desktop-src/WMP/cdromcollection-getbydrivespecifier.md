---
title: CdromCollection. getByDriveSpecifier 方法
description: GetByDriveSpecifier 方法會抓取與特定磁碟機號相關聯的 Cdrom 物件。
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- getByDriveSpecifier 方法 Windows Media Player
- getByDriveSpecifier 方法 Windows Media Player，CdromCollection 類別
- CdromCollection 類別 Windows Media Player，getByDriveSpecifier 方法
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993660"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a>CdromCollection. getByDriveSpecifier 方法

**GetByDriveSpecifier** 方法會抓取與特定磁碟機號相關聯的 **Cdrom** 物件。

## <a name="syntax"></a>語法


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*driveSpecifier* \[在\]
</dt> <dd>

**字串** ，包含後面接著冒號 ( "：" ) 字元的磁碟機號。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回一個 **Cdrom** 物件。

## <a name="remarks"></a>備註

磁碟機號必須以 *x*：形式提供，其中 *X* 代表磁碟機號。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *CdromCollection*。**getByDriveSpecifier** ，以取得對應至使用者所提供之磁碟機號的 **Cdrom** 物件。 已建立 HTML 文字元素，名稱 = "MyText"，用於使用者輸入。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Cdrom 物件**](cdrom-object.md)
</dt> <dt>

[**Cdrom. 退出**](cdrom-eject.md)
</dt> <dt>

[**CdromCollection 物件**](cdromcollection-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






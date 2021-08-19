---
title: IWMPCdromCollection getByDriveSpecifier 方法
description: GetByDriveSpecifier 方法會傳回與特定磁碟機號相關聯的 IWMPCdrom 介面。
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- getByDriveSpecifier 方法 Windows Media Player
- getByDriveSpecifier 方法 Windows Media Player，IWMPCdromCollection 介面
- IWMPCdromCollection 介面 Windows Media Player，getByDriveSpecifier 方法
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9937694234fe7e46fe9b98d83357da19abf18f8d14e83794587f6f2050b0019b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116216"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a>IWMPCdromCollection：： getByDriveSpecifier 方法

**GetByDriveSpecifier** 方法會傳回與特定磁碟機號相關聯的 **IWMPCdrom** 介面。

## <a name="syntax"></a>語法


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrDriveSpecifier* \[在\]
</dt> <dd>

**System.string** ，後面接著冒號 ( "：" ) 字元的磁碟機號。

</dd> </dl>

## <a name="return-value"></a>傳回值

**WMPLib IWMPCdrom** 介面。

## <a name="remarks"></a>備註

磁碟機號必須以 *x*：形式提供，其中 *X* 代表磁碟機號。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會使用 **getByDriveSpecifier** 來取得對應至使用者在文字方塊中所提供之磁碟機號的 **IWMPCdrom** 介面。 接著會呼叫 **IWMPCdrom 取出** 方法來退出指定的磁片磁碟機。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPCdrom 介面 (VB 和 c # )**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPCdrom (VB 和 c # )**](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[**IWMPCdromCollection 介面 (VB 和 c # )**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 






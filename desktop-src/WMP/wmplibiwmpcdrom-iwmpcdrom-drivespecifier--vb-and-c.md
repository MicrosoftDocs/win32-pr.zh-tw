---
title: IWMPCdrom driveSpecifier 屬性
description: DriveSpecifier 屬性會取得 CD 或 DVD 光碟機號。
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- driveSpecifier 屬性 Windows Media Player
- driveSpecifier 屬性 Windows Media Player，IWMPCdrom 介面
- IWMPCdrom 介面 Windows Media Player，driveSpecifier 屬性
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b555cba0ec694a19a01c040a0369aeb473c6811933d45892cbf3c69ef640b8b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031457"
---
# <a name="iwmpcdromdrivespecifier-property"></a>IWMPCdrom：:d riveSpecifier 屬性

**DriveSpecifier** 屬性會取得 CD 或 DVD 光碟機號。

## <a name="syntax"></a>Syntax


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a>屬性值

**System.string** ，表示磁碟機號。

## <a name="remarks"></a>備註

DVD 光碟機通常可以播放 CD 媒體，但 CD 光碟機無法播放 DVD 媒體。

這個屬性會在使用 **IWMPCdromCollection** 抓取的範圍內取得以零為基底之磁片磁碟機索引的磁碟機號。 抓取的值採用 *x*：形式，其中 *X* 代表磁碟機號。

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會使用 **driveSpecifier** 來建立包含可用 CD 和 DVD 光碟機清單的字串，並在訊息方塊中顯示該字串。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
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

[**IWMPCdromCollection (VB 和 c # ) 的計數**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 






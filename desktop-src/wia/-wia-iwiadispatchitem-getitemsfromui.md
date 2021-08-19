---
description: Item 物件的 GetItemsFromUI 方法會顯示一個對話方塊，可讓使用者選取要從裝置傳送的影像和音訊。
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: GetItemsFromUI 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a954dbefec9728d2d6f595144ba3991ab4f7b3a1ded77fdf7e3ca5407be70d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669710"
---
# <a name="itemgetitemsfromui-method"></a>GetItemsFromUI 方法

[**Item**](-wia-item.md)物件的 **GetItemsFromUI** 方法會顯示一個對話方塊，可讓使用者選取要從裝置傳送的影像和音訊。

## <a name="syntax"></a>語法


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **WiaFlag**](-wia-wiaflag.md)**

<dt>



  (0)


</dt> <dd>

預設值。 \[在中， \] 指定對話方塊的行為。 這個參數的有效值與 [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)方法之 *lFlags* 參數的值相同。

</dd> </dl> </dd> <dt>

*意圖* \[在\]
</dt> <dd>

類型： **WiaIntent**

<dt>



  (0)


</dt> <dd>

預設值。 \[中的 \] 指定影像所要代表的資料類型。 如需影像意圖值的清單，請參閱 [**影像意圖常數**](-wia-imageintentconstants.md)。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

類型： **ICollection**

這個方法會傳回代表使用者選取之專案的 [**專案**](-wia-item.md) 物件集合。 如果未選取任何專案，則集合是空的。

## <a name="remarks"></a>備註

針對 Microsoft Visual Basic 的應用程式，請新增「Windows 影像取得1.01 型別程式庫」的參考。

此方法僅適用于)  (根專案的裝置。 方法會傳回代表使用者選取之影像或音訊剪輯的 [**專案**](-wia-item.md) 物件集合。

如果使用者未選取任何專案，則方法會傳回空集合。

## <a name="examples"></a>範例

下列範例示範如何使用 **GetItemsFromUI** 方法，以允許使用者從對話方塊中選取影像。


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 





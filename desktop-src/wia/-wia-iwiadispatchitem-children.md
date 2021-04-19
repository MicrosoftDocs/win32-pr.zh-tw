---
description: Item 物件的子屬性會抓取專案物件的集合。 這個集合中的專案代表在階層樹狀結構中，屬於此專案之直接子系的專案。 唯讀。
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: 專案。子系屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996605"
---
# <a name="itemchildren-property"></a>專案。子系屬性

[**Item**](-wia-item.md)物件的 **子** 屬性會抓取 **專案** 物件的集合。 這個集合中的專案代表在階層樹狀結構中，屬於此專案之直接子系的專案。 唯讀。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Item.Children
```



## <a name="property-value"></a>屬性值

接收物件的變數。

## <a name="remarks"></a>備註

使用這個屬性可流覽代表裝置的 [**專案**](-wia-item.md) 物件階層樹狀結構、資料夾和位於裝置上的檔案。

[ **子** 系] 屬性是 [**專案**](-wia-item.md) 物件的集合，只來自樹狀結構中這個 **專案** 物件下的層級。 若要在樹狀結構中向下導覽層級，請以遞迴方式使用此屬性。

如果專案不能或沒有任何子專案，這個屬性會傳回空集合。

> [!Note]  
> 這個集合是以0為基礎。

 

## <a name="examples"></a>範例

下列範例示範如何使用 [ **子** 系] 屬性來抓取和列舉裝置的子專案集合。 如果裝置是數位相機，則集合通常會包含資料夾和影像專案。 如果裝置是掃描器，則集合通常會包含代表掃描張床的專案。


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 





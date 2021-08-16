---
description: Item 物件的 Transfer 方法會將資料從裝置傳送到檔案。 此方法僅適用于裝置類型專案。
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Transfer 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: efef054a324244553748b75659820f582100a01ed6f56f9a2f80b0ef0c08f105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706318"
---
# <a name="itemtransfer-method"></a>Item. Transfer 方法

[**Item**](-wia-item.md)物件的 **Transfer** 方法會將資料從裝置傳送到檔案。 此方法僅適用于裝置類型專案。

## <a name="syntax"></a>語法


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*檔案名* \[在\]
</dt> <dd>

類型： **BSTR**

指定要將資料傳輸至其中的檔案名。

</dd> <dt>

*AsyncTransfer* \[在\]
</dt> <dd>

Type： **VARIANT \_ BOOL**

布林值，指定是否應該以非同步呼叫來執行傳送。

<dt>



  (VARIANT \_ BOOL) 


</dt> <dd>

預設值。 如果呼叫應該是非同步，請將此值設定為 **true** ， (查看 **備註**) 。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法只適用于檔案類型專案。 方法會先檢查項目是否支援這個方法，然後再嘗試完成資料傳輸。

使用 "剪貼簿" 作為 *Filename* 參數，將專案傳送至剪貼簿。

將 *AsyncTransfer* 值設定為 **false** ，以在任何應用程式或腳本內執行的任何應用程式或腳本中執行，而該環境會在腳本結束時終止進程，例如 Windows 腳本主機 (WSH) 。 否則，腳本可能會結束，且進程會在傳送完成之前終止。

傳送方法沒有 **傳回** 值。 完成傳送時，此方法會將 [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) 事件傳送至腳本或應用程式。

## <a name="examples"></a>範例

下列範例示範如何使用 **傳送** 方法，從裝置傳送資料。


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 





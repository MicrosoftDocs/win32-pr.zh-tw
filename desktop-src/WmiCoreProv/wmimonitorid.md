---
description: 代表影片監視器的識別資訊，例如製造商名稱、製造年份或序號。
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: WmiMonitorID 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 485b42a86ca67d15ec00be13992c17b31ed51608
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106984282"
---
# <a name="wmimonitorid-class"></a>WmiMonitorID 類別

**WmiMonitorID** WMI 類別代表影片監視器的識別資訊，例如製造商名稱、製造年份或序號。 此類別中的資料會對應至視頻電子產品標準關聯之影片輸入定義的廠商/產品識別區塊中的資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 標準。

## <a name="syntax"></a>語法

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a>成員

**WmiMonitorID** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**WmiMonitorID** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示使用中的監視器。

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

特定監視實例的名稱。

</dd> <dt>

**ManufacturerName**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

製造商的名稱。

</dd> <dt>

**ManufacturerNameLength**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

位於 **ManufacturerName** 屬性中的製造商名稱長度。

</dd> <dt>

**ProductCodeID**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

廠商指派的產品代碼識別碼。

</dd> <dt>

**SerialNumberID**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

序號。

</dd> <dt>

UserFriendlyName
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

監視器的易記名稱。 名稱的大小是由 UserFriendlyNameLength 屬性所指定的長度。

</dd> <dt>

UserFriendlyNameLength
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

名稱位於 UserFriendlyName 屬性中的字元數。

</dd> <dt>

**WeekOfManufacture**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

依周數的製造周數。 範圍是從1到53。 未定義零 (0) 。

</dd> <dt>

**YearOfManufacture**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

製造的年。

</dd> </dl>

## <a name="remarks"></a>備註

如需如何轉譯儲存序號識別碼之陣列的討論，請參閱設定管理員 blog 文章中的 [報告監視器資訊](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) 。

## <a name="examples"></a>範例

下列 PowerShell 範例會取出多個監視的序號。


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



下列 VBScript 程式碼也會從系統中取出監視器識別碼資訊。


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 命名空間<br/>                | 根 \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 


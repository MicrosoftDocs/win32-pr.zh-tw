---
description: Win32 \_ 共用類別代表執行 Windows 的電腦系統上的共用資源。 這可能是磁片磁碟機、印表機、處理序間通訊或其他可共用的裝置。 如需有關如何抓取 WMI 類別的詳細資訊，請參閱取出類別。
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Win32_Share 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111204"
---
# <a name="win32_share-class"></a>Win32 \_ 共用類別

**Win32 \_ 共用** 類別代表執行 Windows 的電腦系統上的共用資源。 這可能是磁片磁碟機、印表機、處理序間通訊或其他可共用的裝置。 如需有關如何抓取 WMI 類別的詳細資訊，請參閱 [取出類別](../wmisdk/retrieving-a-class.md)。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
};
```

## <a name="members"></a>成員

**Win32 \_ 共用** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ 共用** 類別具有這些方法。



| 方法                                                             | 描述                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**創建**](create-method-in-class-win32-share.md)               | 起始伺服器資源之共用的類別方法。<br/>                                                                                                                                               |
| [**刪除**](delete-method-in-class-win32-share.md)               | 類別方法，會從伺服器的共用資源清單中刪除共用名稱，中斷與共用資源的連接。<br/>                                                                       |
| [**GetAccessMask**](getaccessmask-method-in-class-win32-share.md) | 傳回使用者或群組所持有的共用的存取權限，該共用會傳回該實例。 您應該使用這個方法來取代 **AccessMask** 屬性，此屬性一律為 **Null**。<br/> |
| [**SetShareInfo**](setshareinfo-method-in-class-win32-share.md)   | 設定共用資源的參數的類別方法。<br/>                                                                                                                                              |



 

### <a name="properties"></a>屬性

**Win32 \_ 共用** 類別具有這些屬性。

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

這個屬性已過時，不再使用。 請改用 [**Win32 \_ GetAccessMask**](getaccessmask-method-in-class-win32-share.md) 方法。 WMI 會將 **AccessMask** 屬性的值設定為 **null** 。 如需在建立共用時設定存取權的詳細資訊，請參閱 [**建立**](create-method-in-class-win32-share.md) 方法。

</dd> <dt>

**AllowMaximum**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ 使用」 ) 
</dt> </dl>

此資源的並行使用者數目已受限制。 若 **為 True**，則會忽略 **MaximumAllowed** 屬性中的值。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) 
</dt> </dl>

物件的文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

指出物件的安裝時間。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**MaximumAllowed**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ 使用」 ) 
</dt> </dl>

允許同時使用此資源的使用者數目上限。 只有當 **AllowMaximum** 屬性設定為 **FALSE** 時，此值才有效。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Name" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**SHARE \_ INFO \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1)shi1 網路名稱 \| \_ " ) 
</dt> </dl>

在執行 Windows 的電腦系統上，提供給路徑的別名設定為共用。

Windows 2008 範例： " \\ SERVER01 \\ public"-windows Server 2008 要求您將 UNC 放在名稱中。

</dd> <dt>

**路徑**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ 路徑」 ) 
</dt> </dl>

Windows 共用的本機路徑。

範例： "C： \\ Program Files"

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
</dt> </dl>

表示物件目前狀態的字串。 您可以定義操作和非運作狀態。 操作狀態可以包含「確定」、「降級」和「Pred 失敗」。 「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。

非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。 「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

包括下列值：

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** ( [確定] ) 


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** ( 「錯誤」 ) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**降級** ( 「降級」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred 失敗** ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**開始** ( 「開始」 ) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**停止** ( 「正在停止」 ) 


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**服務** ( 「服務」 ) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** ( 「壓力」 ) 


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ( "NonRecover" ) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** ( 「沒有連絡人」 ) 


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**遺失的 comm** ( 「遺失的通訊」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**型別**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ 類型」 ) 
</dt> </dl>

共用的資源類型。 類型包括：磁片磁碟機、列印佇列、處理序間通訊 (IPC) 和一般裝置。

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**磁片磁碟機** (0) 


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**列印佇列** (1) 


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**裝置** (2) 


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3) 


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**磁片磁碟機系統管理員** (2147483648) 


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**列印佇列管理** (2147483649) 


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**裝置系統管理員** (2147483650) 


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**IPC 系統管理員** (2147483651) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ 共用** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。

此類別中的 Create 方法是靜態方法。 **Delete**、 **GetAccessMask** 和 **SetShareInfo** 方法都是實例方法。

根據您的安全性許可權，您可能無法取得此類別的所有屬性。 例如， **AllowMaximum**、 **MaximumAllowed**、 **Path** 和 **Type** 屬性可能會傳回 null。 一般來說，Power Users 和系統管理員將能取得所有屬性值。

## <a name="examples"></a>範例

下列腳本中心程式[代碼範例](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) 會列出電腦上的所有共用，並列出每個共用的所有共用許可權。

[Get 共用資訊與 win32 \_ 共用](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c)PowerShell 範例查詢 win32 \_ 共用，並提供結果。

下列 PowerShell 範例會顯示本機系統上的共用。


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



或者，如果您想要更精確地篩選，您可以使用下列 PowerShell 程式碼片段：


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



下列 VBScript 範例會顯示本機系統上的共用。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
Next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> <dt>

[WMI 工作：檔案和資料夾](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 

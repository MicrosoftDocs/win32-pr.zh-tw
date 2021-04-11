---
description: Win32 \_ ClusterShare 類別代表叢集中的共用資源。
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Win32_ClusterShare 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare
- Win32_ClusterShare.Caption
- Win32_ClusterShare.Description
- Win32_ClusterShare.InstallDate
- Win32_ClusterShare.Status
- Win32_ClusterShare.AccessMask
- Win32_ClusterShare.AllowMaximum
- Win32_ClusterShare.MaximumAllowed
- Win32_ClusterShare.Name
- Win32_ClusterShare.Path
- Win32_ClusterShare.Type
- Win32_ClusterShare.ServerName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccff6ad8d99692d066728c99dd74ab07640af4fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111237"
---
# <a name="win32_clustershare-class"></a>Win32 \_ ClusterShare 類別

\[**Win32 \_ ClusterShare** 類別已被取代。 請改用 [**msft 檔案 \_ 共用**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) 和 [**msft \_ SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) 類別。\]

Win32 \_ ClusterShare 類別代表叢集中的共用資源。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_ClusterShare : Win32_Share
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
  string   ServerName;
};
```

## <a name="members"></a>成員

**Win32 \_ ClusterShare** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ ClusterShare** 類別具有這些方法。



| 方法                                                    | 描述                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [**創建**](create-win32-clustershare.md)               | 建立新的 **Win32 \_ ClusterShare** 實例。<br/>       |
| [**刪除**](delete-win32-clustershare.md)               | 刪除 **Win32 \_ ClusterShare** 實例。<br/>           |
| [**GetAccessMask**](getaccessmask-win32-clustershare.md) | 傳回具有共用存取權限的點陣圖。<br/> |
| [**SetShareInfo**](setshareinfo-win32-clustershare.md)   | 設定共用資源的參數。<br/>           |



 

### <a name="properties"></a>屬性

**Win32 \_ ClusterShare** 類別具有這些屬性。

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

這個屬性已過時，不再使用。 請改用 [**Win32 \_ GetAccessMask**](getaccessmask-method-in-class-win32-share.md) 方法。 WMI 會將 **AccessMask** 屬性的值設定為 **null** 。 如需在建立共用時設定存取權的詳細資訊，請參閱 [**建立**](create-method-in-class-win32-share.md) 方法。

這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。

</dd> <dt>

**AllowMaximum**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ 使用」 ) 
</dt> </dl>

此資源的並行使用者數目已受限制。 若 **為 True**，則會忽略 **MaximumAllowed** 屬性中的值。

這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) 
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

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) 
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

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") 
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

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ 使用」 ) 
</dt> </dl>

允許同時使用此資源的使用者數目上限。 只有當 **AllowMaximum** 屬性設定為 **FALSE** 時，此值才有效。

這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| shi1 網路名稱」 \_ ) 
</dt> </dl>

在執行 Windows 的電腦系統上，提供給路徑的別名設定為共用。

Windows 2008 範例： " \\ SERVER01 \\ public"-windows Server 2008 要求您將 UNC 放在名稱中。

這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。

</dd> <dt>

**路徑**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ 路徑」 ) 
</dt> </dl>

Windows 共用的本機路徑。

範例： "C： \\ Program Files"

這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ServerName" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Network Management 結構 \| [**SHARE \_ INFO \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| shi503 \_ ServerName" ) 
</dt> </dl>

主控共用的叢集伺服器。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
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

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 網路管理結構 \| [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ 類型」 ) 
</dt> </dl>

共用的資源類型。 類型包括：磁片磁碟機、列印佇列、處理序間通訊 (IPC) 和一般裝置。

這個屬性繼承自 [**Win32 \_ 共用**](win32-share.md)。

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

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                       |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ 共用**](win32-share.md)
</dt> </dl>

 


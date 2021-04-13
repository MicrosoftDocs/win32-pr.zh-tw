---
title: Win32_RDCentralPublishedRemoteDesktop 類別
description: 在另一部電腦上發佈的桌面，可透過終端機服務進行遠端使用。
ms.assetid: 2b28a2d3-048f-446f-9ce0-eb684b393eaa
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedRemoteDesktop 類別遠端桌面服務
- Win32_RDCentralPublishedRemoteDesktop 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteDesktop
- Win32_RDCentralPublishedRemoteDesktop.Caption
- Win32_RDCentralPublishedRemoteDesktop.Description
- Win32_RDCentralPublishedRemoteDesktop.InstallDate
- Win32_RDCentralPublishedRemoteDesktop.Name
- Win32_RDCentralPublishedRemoteDesktop.Status
- Win32_RDCentralPublishedRemoteDesktop.PublishingFarm
- Win32_RDCentralPublishedRemoteDesktop.Alias
- Win32_RDCentralPublishedRemoteDesktop.IconContents
- Win32_RDCentralPublishedRemoteDesktop.ShowInPortal
- Win32_RDCentralPublishedRemoteDesktop.RDPFileContents
- Win32_RDCentralPublishedRemoteDesktop.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04696331b7027b7cc65d2202c29e6ce95bb3f4b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464969"
---
# <a name="win32_rdcentralpublishedremotedesktop-class"></a>Win32 \_ RDCentralPublishedRemoteDesktop 類別

在另一部電腦上發佈的桌面，可透過終端機服務進行遠端使用

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a>成員

**Win32 \_ RDCentralPublishedRemoteDesktop** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ RDCentralPublishedRemoteDesktop** 類別具有這些屬性。

<dl> <dt>

**別名**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

桌面的別名。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

簡短描述 (物件的單行字串) 。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**資料夾**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

應顯示此資源的資料夾清單。

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

對應到應用程式的圖示內容。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") 
</dt> </dl>

物件的安裝日期。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的名稱。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**PublishingFarm**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

發佈桌面之伺服器陣列的別名。

</dd> <dt>

**RDPFileContents**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對應于桌面之 RDP 檔案的內容。

</dd> <dt>

**ShowInPortal**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如果此應用程式應該顯示在 TS Web 存取中，則 **為 true** ;否則 **為 false**。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

<dt>



  ( [確定] ) 


</dt> <dd></dd> <dt>



  ( 「錯誤」 ) 


</dt> <dd></dd> <dt>



  ( 「降級」 ) 


</dt> <dd></dd> <dt>



  ( 「未知」 ) 


</dt> <dd></dd> <dt>



  ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>



  ( 「開始」 ) 


</dt> <dd></dd> <dt>



  ( 「正在停止」 ) 


</dt> <dd></dd> <dt>



  ( "Service" ) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                           |
| 命名空間<br/>                | 根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Tscpub mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 


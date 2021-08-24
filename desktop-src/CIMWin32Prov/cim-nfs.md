---
description: CIM \_ NFS 類別代表從電腦系統使用網路檔案系統 (NFS) 通訊協定掛接的遠端檔案系統。
ms.assetid: 24eba28f-fbd5-4aa3-a7c7-a611269d55ac
ms.tgt_platform: multiple
title: CIM_NFS 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NFS
- CIM_NFS.AttributeCaching
- CIM_NFS.AttributeCachingForDirectoriesMax
- CIM_NFS.AttributeCachingForDirectoriesMin
- CIM_NFS.AttributeCachingForRegularFilesMax
- CIM_NFS.AttributeCachingForRegularFilesMin
- CIM_NFS.AvailableSpace
- CIM_NFS.BlockSize
- CIM_NFS.Caption
- CIM_NFS.CasePreserved
- CIM_NFS.CaseSensitive
- CIM_NFS.CodeSet
- CIM_NFS.CompressionMethod
- CIM_NFS.CreationClassName
- CIM_NFS.CSCreationClassName
- CIM_NFS.CSName
- CIM_NFS.Description
- CIM_NFS.EncryptionMethod
- CIM_NFS.FileSystemSize
- CIM_NFS.ForegroundMount
- CIM_NFS.HardMount
- CIM_NFS.InstallDate
- CIM_NFS.Interrupt
- CIM_NFS.MaxFileNameLength
- CIM_NFS.MountFailureRetries
- CIM_NFS.Name
- CIM_NFS.ReadBufferSize
- CIM_NFS.ReadOnly
- CIM_NFS.RetransmissionAttempts
- CIM_NFS.RetransmissionTimeout
- CIM_NFS.Root
- CIM_NFS.ServerCommunicationPort
- CIM_NFS.Status
- CIM_NFS.WriteBufferSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cfdf044adf5623a7fafd424f6051105bf83d3d0f5f4338b16b7bf3a7fe07126c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820968"
---
# <a name="cim_nfs-class"></a>CIM \_ NFS 類別

**CIM \_ NFS** 類別代表從電腦系統使用網路檔案系統 (NFS) 通訊協定掛接的遠端檔案系統。 NFS 物件的屬性會對應至掛接的操作方面，並代表 NFS 存取的用戶端設定。 檔案系統類型應該設定為指出檔案系統出現在用戶端的類型。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{75BCF4FB-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_NFS : CIM_RemoteFileSystem
{
  boolean  AttributeCaching;
  uint16   AttributeCachingForDirectoriesMax;
  uint16   AttributeCachingForDirectoriesMin;
  uint16   AttributeCachingForRegularFilesMax;
  uint16   AttributeCachingForRegularFilesMin;
  uint64   AvailableSpace;
  uint64   BlockSize;
  string   Caption;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  boolean  ForegroundMount;
  boolean  HardMount;
  datetime InstallDate;
  boolean  Interrupt;
  uint32   MaxFileNameLength;
  uint16   MountFailureRetries;
  string   Name;
  uint64   ReadBufferSize;
  boolean  ReadOnly;
  uint16   RetransmissionAttempts;
  uint32   RetransmissionTimeout;
  string   Root;
  uint32   ServerCommunicationPort;
  string   Status;
  uint64   WriteBufferSize;
};
```

## <a name="members"></a>成員

**CIM \_ NFS** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ NFS** 類別具有這些屬性。

<dl> <dt>

**AttributeCaching**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則會啟用控制項屬性快取。 如果 **為 FALSE**，則會停用控制項屬性快取。

</dd> <dt>

**AttributeCachingForDirectoriesMax**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) 
</dt> </dl>

目錄更新後保存快取屬性的最大秒數。

</dd> <dt>

**AttributeCachingForDirectoriesMin**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) 
</dt> </dl>

目錄更新後保存快取屬性的最小秒數。

</dd> <dt>

**AttributeCachingForRegularFilesMax**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) 
</dt> </dl>

檔案修改後保存快取屬性的最大秒數。

</dd> <dt>

**AttributeCachingForRegularFilesMin**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) 
</dt> </dl>

檔案修改後保存快取屬性的最小秒數。

</dd> <dt>

**AvailableSpace**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.4 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") 
</dt> </dl>

檔案系統的可用空間總量（以位元組為單位）。 如果不明，請輸入0。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) 
</dt> </dl>

檔案系統可以讀取或寫入個別于基礎儲存範圍之外定義之區塊中的資料。 這個屬性會針對資料儲存和抓取來捕捉檔案系統的區塊大小。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

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

**CasePreserved**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則會保留檔案名的大小寫。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

</dd> <dt>

**CaseSensitive**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則支援區分大小寫的檔案名。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

檔案系統支援的字元集或編碼。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

**ASCII** (2) 


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

**Unicode** (3) 


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

**ISO2022** (4) 


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

**ISO8859** (5) 


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

**擴充 UNIX 程式碼** (6) 


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

**Utf-8** (7) 


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

**UCS-2** (8) 


</dt> <dd></dd> </dl>

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.7」 ) 
</dt> </dl>

自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。 如果壓縮配置未知或未描述，請使用「未知」。 如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。 如果邏輯檔案未壓縮，請使用「未壓縮」。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未產生」。**CreationClassName**") 
</dt> </dl>

設定電腦系統建立類別名稱的範圍。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未產生」。**名稱**") 
</dt> </dl>

設定電腦系統名稱的範圍。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

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

**EncryptionMethod**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 分割區 \| 002.8」 ) 
</dt> </dl>

識別用來加密邏輯檔案之演算法或工具的自由格式字串。 如果未 indulged 加密配置 (基於安全性理由（例如) ），請使用「未知」。 如果檔案已加密，但其加密配置不明或未洩漏，請使用「加密」。 如果邏輯檔案未加密，請使用「未加密」。 這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

</dd> <dt>

**FileSystemSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) 
</dt> </dl>

檔案系統的大小總計（以位元組為單位）。 如果不明，請輸入 0 (零) 。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**ForegroundMount**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則會在前景中執行重試。 如果 **為 FALSE**，且第一次掛接嘗試失敗，則會在背景中執行重試。

</dd> <dt>

**HardMount**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，裝載檔案系統之後，就會重試 NFS 要求，直到主機系統回應為止。 如果 **為 FALSE**，則掛接檔案系統之後，如果裝載系統沒有回應，就會傳回錯誤。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") 
</dt> </dl>

物件的安裝日期和時間。 這個屬性不需要值來表示已安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**中斷**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若為 **TRUE**，則允許進行硬掛接的中斷。 如果 **為 FALSE**，則會忽略硬掛接的中斷。

</dd> <dt>

**MaxFileNameLength**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

檔案系統內檔案名的最大長度。 值為 0 (零) 表示檔案名的長度沒有限制。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

</dd> <dt>

**MountFailureRetries**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

允許的掛接失敗重試次數上限。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 
</dt> </dl>

已知物件的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**ReadBufferSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) 
</dt> </dl>

讀取緩衝區大小（以位元組為單位）。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**ReadOnly**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrFSAccess ") 
</dt> </dl>

若 **為 TRUE**，則會將檔案系統指定為唯讀。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

</dd> <dt>

**RetransmissionAttempts**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

允許的 NFS 重新傳輸數目上限。

</dd> <dt>

**RetransmissionTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「十分之一秒」 ) 
</dt> </dl>

NFS 超時，以十分之一秒為限。

</dd> <dt>

**Root**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrFSMountPoint ") 
</dt> </dl>

定義檔案系統根目錄的路徑名稱或其他資訊。

這個屬性繼承自 [**CIM \_ 檔案系統**](cim-filesystem.md)。

</dd> <dt>

**ServerCommunicationPort**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端電腦系統的 UDP 埠號碼。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
</dt> </dl>

物件的目前狀態。

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

**WriteBufferSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) 
</dt> </dl>

寫入緩衝區大小（以位元組為單位）。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ NFS** 類別衍生自 [**cim \_ RemoteFileSystem**](cim-remotefilesystem.md)。

WMI 不會執行這個類別。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

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

[**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md)
</dt> </dl>

 


---
title: Win32_RDCentralPublishedDeploymentSettings 類別
description: 包含用來為從伺服器陣列發佈的資源產生 RDP 檔案的部署設定。
ms.assetid: 6d1be0b2-e070-4c60-8068-b59ba121bf9f
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedDeploymentSettings 類別遠端桌面服務
- Win32_RDCentralPublishedDeploymentSettings 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedDeploymentSettings
- Win32_RDCentralPublishedDeploymentSettings.Caption
- Win32_RDCentralPublishedDeploymentSettings.Description
- Win32_RDCentralPublishedDeploymentSettings.InstallDate
- Win32_RDCentralPublishedDeploymentSettings.Name
- Win32_RDCentralPublishedDeploymentSettings.Status
- Win32_RDCentralPublishedDeploymentSettings.PublishingFarm
- Win32_RDCentralPublishedDeploymentSettings.Port
- Win32_RDCentralPublishedDeploymentSettings.FarmName
- Win32_RDCentralPublishedDeploymentSettings.GatewayUsage
- Win32_RDCentralPublishedDeploymentSettings.GatewayName
- Win32_RDCentralPublishedDeploymentSettings.GatewayAuthMode
- Win32_RDCentralPublishedDeploymentSettings.GatewayUseCachedCreds
- Win32_RDCentralPublishedDeploymentSettings.ColorBitDepth
- Win32_RDCentralPublishedDeploymentSettings.AllowFontSmoothing
- Win32_RDCentralPublishedDeploymentSettings.UseMultimon
- Win32_RDCentralPublishedDeploymentSettings.RedirectionOptions
- Win32_RDCentralPublishedDeploymentSettings.HasCertificate
- Win32_RDCentralPublishedDeploymentSettings.CertificateHash
- Win32_RDCentralPublishedDeploymentSettings.CustomRDPSettings
- Win32_RDCentralPublishedDeploymentSettings.DeploymentRDPSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b118f2fabf22f10e47c0b8467b0ddf6388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385162"
---
# <a name="win32_rdcentralpublisheddeploymentsettings-class"></a>Win32 \_ RDCentralPublishedDeploymentSettings 類別

包含用來為從伺服器陣列發佈的資源產生 RDP 檔案的部署設定。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a>成員

**Win32 \_ RDCentralPublishedDeploymentSettings** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ RDCentralPublishedDeploymentSettings** 類別具有這些屬性。

<dl> <dt>

**AllowFontSmoothing**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

**true** 表示允許字型平滑;否則 **為 false**。

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

**CertificateHash**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

用來簽署 RDP 檔案的憑證;只有當 *HasCertificate* 為 true 時，才必須如此。

</dd> <dt>

**ColorBitDepth**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

包含色彩位深度：

<dt>

<span id="4"></span>

**4** () 


</dt> <dd></dd> <dt>

<span id="8"></span>

**8** () 


</dt> <dd></dd> <dt>

<span id="15"></span>

**15** () 


</dt> <dd></dd> <dt>

<span id="16"></span>

**16** () 


</dt> <dd></dd> <dt>

<span id="24"></span>

**24** () 


</dt> <dd></dd> <dt>

<span id="32"></span>

**32** () 


</dt> <dd></dd> </dl>

</dd> <dt>

**CustomRDPSettings**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

包含對應至自訂 RDP 設定的 RDP 檔案內容。

</dd> <dt>

**DeploymentRDPSettings**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

包含對應至部署設定之 RDP 檔案的內容。 如果設定此參數，系統將會使用這個 RDP 檔案，並忽略此呼叫中的其他 RDP 設定。

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

**FarmName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

伺服器陣列的名稱。

</dd> <dt>

**GatewayAuthMode**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

包含閘道驗證模式：

<dt>

<span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>

<span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**密碼 (0)** (0) 


</dt> <dd></dd> <dt>

<span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>

<span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**智慧卡 (1)** (1) 


</dt> <dd></dd> <dt>

<span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>

<span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**允許使用者選擇 (4)** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**GatewayName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

閘道器的名稱。

</dd> <dt>

**GatewayUsage**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

說明如何使用閘道：

<dt>

<span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>

<span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**NoGateway** (0) 


</dt> <dd>

沒有閘道。

</dd> <dt>

<span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>

<span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1) 


</dt> <dd>

使用本機閘道傳遞。

</dd> <dt>

<span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>

<span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2) 


</dt> <dd>

使用閘道。

</dd> <dt>

<span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>

<span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3) 


</dt> <dd>

偵測閘道。

</dd> </dl>

</dd> <dt>

**GatewayUseCachedCreds**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

**true** 表示盡可能使用 ts 閘道和 ts 伺服器的相同使用者認證;否則 **為 false**。

</dd> <dt>

**HasCertificate**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

**true** 表示使用憑證來簽署 RDP 檔案;否則 **為 false**。

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

**通訊埠**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RDP 埠。

</dd> <dt>

**PublishingFarm**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

發佈應用程式之伺服器陣列的別名。

</dd> <dt>

**RedirectionOptions**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

重新導向選項：

<dt>

0
</dt> <dd>

無

</dd> <dt>

1
</dt> <dd>

磁碟機

</dd> <dt>

2
</dt> <dd>

印表機

</dd> <dt>

4
</dt> <dd>

剪貼簿

</dd> <dt>

8
</dt> <dd>

隨插即用

</dd> <dt>

16
</dt> <dd>

智慧卡

</dd> </dl>

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

</dd> <dt>

**UseMultimon**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

**true** 表示啟用桌面的多重監視器 (不使用滑軌) ;否則 **為 false**。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                           |
| 命名空間<br/>                | 根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Tscpub mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 


---
title: Win32_TSDeploymentSettings 類別
description: 定義 RemoteApp 管理員在建立遠端桌面通訊協定 (RDP) 檔案時所使用的預設設定。
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentSettings 類別遠端桌面服務
- Win32_TSDeploymentSettings 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f5b5cde779cbd9b8120fa648138611236935080f3517a28a6f19dcee8864b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349306"
---
# <a name="win32_tsdeploymentsettings-class"></a>Win32 \_ TSDeploymentSettings 類別

定義 RemoteApp 管理員在建立遠端桌面通訊協定 (RDP) 檔案時所使用的預設設定。 這些設定不會影響任何已發佈的應用程式或桌上型電腦。

## <a name="syntax"></a>語法

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a>成員

**Win32 \_ TSDeploymentSettings** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ TSDeploymentSettings** 類別具有這些屬性。

<dl> <dt>

**AllowFontSmoothing**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否允許字型平滑。

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

**CertificateExpiresOn**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

憑證到期的日期。 此值會儲存為64位 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 格式。

</dd> <dt>

**CertificateHash**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

用來簽署 RDP 檔案的憑證指紋。

</dd> <dt>

**CertificateIssuedBy**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定憑證的簽發者。

</dd> <dt>

**CertificateIssuedTo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定憑證的發行物件。

</dd> <dt>

**ColorBitDepth**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

顯示器的色彩位深度。 可能的值為4、8、15、16、24和32。

</dd> <dt>

**CustomRDPSettings**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RDP 檔案的內容，對應至 RemoteApp 管理員中的自訂 RDP 設定。

</dd> <dt>

**DeploymentRDPSettings**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RDP 檔案的內容，對應至 RemoteApp 管理員中的部署設定。 如果設定此值，RDP 部署設定會取代此類別中的預設設定。 例如，如果您在這個類別中設定 **GatewayAuthMode** 屬性，並設定 **DeploymentRDPSettings** 屬性，則會忽略這個類別的 **GatewayAuthMode** 屬性，並使用 **DeploymentRDPSettings** 的 **GatewayAuthMode** 值。

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

RD 工作階段主機伺服器的名稱，或 RD 工作階段主機伺服器陣列 (FQDN) 的完整功能變數名稱。

</dd> <dt>

**GatewayAuthMode**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 閘道的驗證方法。 可能的值如下。

<dt>

0
</dt> <dd>

密碼

</dd> <dt>

1
</dt> <dd>

智慧卡

</dd> <dt>

4
</dt> <dd>

允許使用者在連接期間進行選取。

</dd> </dl>

</dd> <dt>

**GatewayName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

要使用 RD 閘道伺服器的名稱。

</dd> <dt>

**GatewayUsage**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否要使用 RD 閘道伺服器來連接到整個防火牆的目標 RD 工作階段主機伺服器。 可能的值如下。

<dt>

0
</dt> <dd>

請勿使用 RD 閘道的伺服器。

</dd> <dt>

1
</dt> <dd>

使用 RD 閘道 server。 略過本機位址的 RD 閘道 server。

</dd> <dt>

2
</dt> <dd>

使用 RD 閘道 server。

</dd> <dt>

3
</dt> <dd>

自動偵測 RD 閘道伺服器設定。

</dd> </dl>

</dd> <dt>

**GatewayUseCachedCreds**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

可能的話，請針對 RD 閘道伺服器和 RD 工作階段主機伺服器使用相同的使用者認證。

</dd> <dt>

**HasCertificate**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否要使用憑證來簽署 RDP 檔案。

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

要使用的 RDP 埠。

</dd> <dt>

**RedirectionOptions**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定 RemoteApp 連接的裝置和資源重新導向選項。 可以結合 **RedirectionOptions** 的旗標。 可能的值如下。

<dt>

0
</dt> <dd>

無裝置或資源重新導向。

</dd> <dt>

1
</dt> <dd>

重新導向磁片磁碟機。

</dd> <dt>

2
</dt> <dd>

重新導向印表機。

</dd> <dt>

4
</dt> <dd>

重新導向剪貼簿。

</dd> <dt>

8
</dt> <dd>

重新導向支援的隨插即用裝置。

</dd> <dt>

16
</dt> <dd>

重新導向智慧卡。

</dd> <dt>

32
</dt> <dd>

重新導向音訊。

</dd> <dt>

64
</dt> <dd>

重新導向序列埠。

</dd> </dl>

</dd> <dt>

**RequireServerAuth**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否需要伺服器驗證。

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

指出是否已啟用桌面的多個監視器。

</dd> </dl>

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能使用這個類別來設定屬性。

如果 **RequireServerAuth** 設定為 **TRUE**，請考慮下列事項：

-   如果 RemoteApp 程式適用于內部網路，且所有用戶端電腦都執行 Windows Server 2008 或 Windows Vista，您就不需要將 RD 工作階段主機伺服器設定為使用 SSL 憑證。 在此案例中，是使用網路層級驗證。
-   您必須為 **FarmName** 屬性的值指定伺服器或伺服器陣列的 FQDN。

若要連接到 "CIMV2 \\ microsoft-windows-terminalservices-gateway" 命名空間，驗證層級必須包含封包隱私權。 針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級，可以使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM 函式來設定。 針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。 下列 Visual Basic 腳本撰寫版 (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 當您新增相關聯的角色時，它們會安裝在電腦上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 


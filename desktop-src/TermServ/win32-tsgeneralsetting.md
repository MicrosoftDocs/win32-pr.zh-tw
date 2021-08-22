---
title: Win32_TSGeneralSetting 類別
description: 代表終端機的一般設定，例如加密層級和傳輸通訊協定。
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Win32_TSGeneralSetting 類別遠端桌面服務
- Win32_TSGeneralSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2cc2e7ede46b503e0d33f65c5735d5e0cc653a75184384be2d706bfc8ac9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999808"
---
# <a name="win32_tsgeneralsetting-class"></a>Win32 \_ TSGeneralSetting 類別

**Win32 \_ TSGeneralSetting** WMI 類別代表終端機的一般設定，例如加密層級和傳輸通訊協定。

下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。 如需方法的參考資訊，請參閱本主題稍後的方法表格。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a>成員

**Win32 \_ TSGeneralSetting** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSGeneralSetting** 類別具有這些方法。



| 方法                                                                                        | 描述                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)                       | 設定加密層級。<br/>                                                                                                                                   |
| [**SetSecurityLayer**](win32-tsgeneralsetting-setsecuritylayer.md)                           | 將安全性層級設定為「RDP 安全性層級」 (0) 、「Negotiate」 (1) 或「SSL」 (2) 。<br/>                                                                   |
| [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) | 藉由設定 **UserAuthenticationRequired** 屬性的值，啟用或停用使用者必須在連接時驗證的要求。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ TSGeneralSetting** 類別具有這些屬性。

<dl> <dt>

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

**CertificateName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

本機電腦個人憑證主體名稱的顯示名稱。

</dd> <dt>

**憑證**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含已序列化的憑證存放區，其中包含電腦上 [ **我的使用者帳戶** ] 存放區中的所有憑證，該電腦上的憑證與安全通訊端層 (SSL) 搭配使用的有效伺服器憑證。

</dd> <dt>

**註解**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

工作階段層和傳輸通訊協定組合的描述性名稱。

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

**MinEncryptionLevel**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **低** ( 「只有從用戶端傳送到伺服器的資料，會根據伺服器的標準索引鍵強度，以加密來保護。 未保護從伺服器傳送到用戶端的資料。」) ， **中型** ( 「伺服器與用戶端之間傳送的所有資料都是根據伺服器的標準索引鍵強度來受到加密保護」。) ， **高** ( 「伺服器與用戶端之間傳送的所有資料都受到以加密為基礎 onserver 的最大金鑰強度」所保護。) 
</dt> </dl>

最小加密層級。

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**低** (1) 


</dt> <dd>

低層級的加密。 只有從用戶端傳送到伺服器的資料會使用56位加密進行加密。 請注意，從伺服器傳送到用戶端的資料並未加密。

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**中型/用戶端相容** (2) 


</dt> <dd>

用戶端相容的加密層級。 從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會以用戶端所支援的最大金鑰強度進行加密。

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**高** (3) 


</dt> <dd>

高層級的加密。 從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會使用強式128位加密進行加密。 無法連接不支援此加密層級的用戶端。

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**符合 FIPS 規範** 的 (4) 


</dt> <dd>

符合 FIPS 規範的加密。 從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會使用 Microsoft 密碼編譯模組，以聯邦資訊處理標準 (FIPS) 加密演算法進行加密和解密。 FIPS 是「密碼編譯模組的安全性需求」的標準。 FIPS 140-1 (1994) 和 FIPS 140-2 (2001) 描述美國政府內所使用之硬體和軟體密碼編譯模組的政府需求。

</dd> </dl>

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

**PolicySourceMinEncryptionLevel**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **MinEncryptionLevel** 屬性是由伺服器、依群組原則或依預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceSecurityLayer**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **SecurityLayer** 屬性是由伺服器、依群組原則或依預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceUserAuthenticationRequired**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **UserAuthenticationRequired** 屬性是由伺服器、依群組原則或依預設設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> <dt>

2 (0x2) 
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**SecurityLayer**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **RDPSecurityLayer** ( "RDP Security Layer： serverand 之間的通訊，用戶端會使用原生 RDP 加密」。) ， **Negotiate** (」將會使用用戶端支援的最安全層。如果支援，則會使用 TLS 1.0。」) ， **ssl** ( SSL (TLS 1.0) 將用於伺服器驗證，以及 forencrypting 伺服器與用戶端之間傳送的所有資料。此設定需要伺服器具有 SSL 相容的憑證。」) ， **NEWTBD** ( 「LONGHORN 中的新安全層」。) 
</dt> </dl>

指定用戶端與伺服器之間使用的安全性層級。

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP 安全性層** (1) 


</dt> <dd>

伺服器與用戶端之間的通訊會使用原生 RDP 加密。

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**協商** (2) 


</dt> <dd>

使用用戶端支援的最安全層。 如果支援，則會使用 SSL (TLS 1.0) 。

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (3) 


</dt> <dd>

SSL (TLS 1.0) 用於伺服器驗證，以及加密伺服器與用戶端之間傳送的所有資料。 此設定需要伺服器具有 SSL 相容的憑證。 這項設定與 **MinEncryptionLevel** 值1不相容。

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4) 


</dt> <dd>

新的安全性層級。

</dd> </dl>

</dd> <dt>

**SSLCertificateSHA1Hash**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

以 SSL 憑證的十六進位格式來指定要使用之目標伺服器的 SHA1 雜湊。

您可以使用 [憑證內容] 頁面的 [詳細資料] 索引標籤上的 [憑證] MMC 嵌入式管理單元，找到憑證的憑證指紋。

</dd> <dt>

**SSLCertificateSHA1HashType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示 **SSLCertificateSHA1Hash** 屬性的狀態。

<dt>

0 (0x0) 
</dt> <dd>

無效

</dd> <dt>

1 (0x1) 
</dt> <dd>

預設自我簽署

</dd> <dt>

2 (0x2) 
</dt> <dd>

已強制執行預設群組原則

</dd> <dt>

3 (0x3) 
</dt> <dd>

自訂

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

**TerminalName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

終端機的名稱。

這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。

</dd> <dt>

**TerminalProtocol**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

工作階段層通訊協定的名稱;例如，Microsoft RDP 5.0。

</dd> <dt>

**傳輸**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

連接中使用的傳輸類型;例如，TCP、NetBIOS 或 IPX/SPX。

</dd> <dt>

**UserAuthenticationRequired**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定用於遠端連線的使用者驗證類型。 如果設定為1，表示已啟用， **UserAuthenticationRequired** 需要在連接時進行使用者驗證，以增加伺服器保護以防止網路攻擊。 只有支援 RDP 6.0 版或更高版本的 [遠端桌面通訊協定](remote-desktop-protocol.md) (rdp) 用戶端才能連接。 為了避免遠端使用者中斷，建議您在啟用屬性之前，先部署支援適當通訊協定版本的 RDP 用戶端。

您可以使用 [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) 方法來啟用或停用這個屬性。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

連接時的使用者驗證已停用。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

在連接時啟用使用者驗證。

</dd> </dl>

</dd> <dt>

**WindowsAuthentication**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定連接是否預設為標準 Windows 驗證程式或已安裝在系統上的另一個驗證套件。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

不會預設為標準 Windows 驗證進程。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

預設為標準 Windows 驗證進程。

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

請注意，未與主控台會話相關聯的視窗工作站無法存取此類別的方法和屬性。 如果嘗試將 "Console" 指定為 TerminalName 屬性的值，則此物件的方法會傳回 **\_ \_ 不 \_ 支援的 WBEM E**。 如果視窗工作站嘗試呼叫此物件的方法，以新增或修改 LocalSystem、LocalService 或 NetworkService 帳戶的安全性屬性，則也會傳回此錯誤碼。

若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。 針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。 針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。 下列 Visual Basic 腳本撰寫版 (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> </dl>

 


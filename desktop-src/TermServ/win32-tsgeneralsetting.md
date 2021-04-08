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
ms.openlocfilehash: 172f18bbddd364d74dfcfb00e7e665628267af36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685976"
---
# <a name="win32_tsgeneralsetting-class"></a><span data-ttu-id="bc31f-105">Win32 \_ TSGeneralSetting 類別</span><span class="sxs-lookup"><span data-stu-id="bc31f-105">Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="bc31f-106">**Win32 \_ TSGeneralSetting** WMI 類別代表終端機的一般設定，例如加密層級和傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bc31f-106">The **Win32\_TSGeneralSetting** WMI class represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

<span data-ttu-id="bc31f-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bc31f-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="bc31f-108">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="bc31f-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc31f-109">語法</span><span class="sxs-lookup"><span data-stu-id="bc31f-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="bc31f-110">成員</span><span class="sxs-lookup"><span data-stu-id="bc31f-110">Members</span></span>

<span data-ttu-id="bc31f-111">**Win32 \_ TSGeneralSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bc31f-111">The **Win32\_TSGeneralSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="bc31f-112">方法</span><span class="sxs-lookup"><span data-stu-id="bc31f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="bc31f-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bc31f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bc31f-114">方法</span><span class="sxs-lookup"><span data-stu-id="bc31f-114">Methods</span></span>

<span data-ttu-id="bc31f-115">**Win32 \_ TSGeneralSetting** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="bc31f-115">The **Win32\_TSGeneralSetting** class has these methods.</span></span>



| <span data-ttu-id="bc31f-116">方法</span><span class="sxs-lookup"><span data-stu-id="bc31f-116">Method</span></span>                                                                                        | <span data-ttu-id="bc31f-117">描述</span><span class="sxs-lookup"><span data-stu-id="bc31f-117">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc31f-118">**SetEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="bc31f-118">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)                       | <span data-ttu-id="bc31f-119">設定加密層級。</span><span class="sxs-lookup"><span data-stu-id="bc31f-119">Sets the encryption level.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="bc31f-120">**SetSecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="bc31f-120">**SetSecurityLayer**</span></span>](win32-tsgeneralsetting-setsecuritylayer.md)                           | <span data-ttu-id="bc31f-121">將安全性層級設定為「RDP 安全性層級」 (0) 、「Negotiate」 (1) 或「SSL」 (2) 。</span><span class="sxs-lookup"><span data-stu-id="bc31f-121">Sets the security layer to one of "RDP Security Layer" (0), "Negotiate" (1), or "SSL" (2).</span></span><br/>                                                                   |
| [<span data-ttu-id="bc31f-122">**SetUserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="bc31f-122">**SetUserAuthenticationRequired**</span></span>](setuserauthenticationrequired-win32-tsgeneralsetting.md) | <span data-ttu-id="bc31f-123">藉由設定 **UserAuthenticationRequired** 屬性的值，啟用或停用使用者必須在連接時驗證的要求。</span><span class="sxs-lookup"><span data-stu-id="bc31f-123">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bc31f-124">屬性</span><span class="sxs-lookup"><span data-stu-id="bc31f-124">Properties</span></span>

<span data-ttu-id="bc31f-125">**Win32 \_ TSGeneralSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bc31f-125">The **Win32\_TSGeneralSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc31f-126">**標題**</span><span class="sxs-lookup"><span data-stu-id="bc31f-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc31f-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-129">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="bc31f-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-130">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="bc31f-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="bc31f-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bc31f-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-132">**CertificateName**</span><span class="sxs-lookup"><span data-stu-id="bc31f-132">**CertificateName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc31f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-135">本機電腦個人憑證主體名稱的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="bc31f-135">Display name for the local computer personal certificate subject name.</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-136">**憑證**</span><span class="sxs-lookup"><span data-stu-id="bc31f-136">**Certificates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-137">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="bc31f-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-139">包含已序列化的憑證存放區，其中包含電腦上 [ **我的使用者帳戶** ] 存放區中的所有憑證，該電腦上的憑證與安全通訊端層 (SSL) 搭配使用的有效伺服器憑證。</span><span class="sxs-lookup"><span data-stu-id="bc31f-139">Contains a serialized certificate store that contains all of the certificates from the **My user account** store on the computer that are valid server certificates for use with secure sockets layer (SSL).</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-140">**註解**</span><span class="sxs-lookup"><span data-stu-id="bc31f-140">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc31f-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bc31f-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-143">工作階段層和傳輸通訊協定組合的描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="bc31f-143">Descriptive name of the combination of session layer and transport protocol.</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-144">**說明**</span><span class="sxs-lookup"><span data-stu-id="bc31f-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc31f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-147">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="bc31f-147">Description of the object.</span></span>

<span data-ttu-id="bc31f-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bc31f-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bc31f-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-150">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="bc31f-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-152">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="bc31f-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-153">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="bc31f-153">The date the object was installed.</span></span> <span data-ttu-id="bc31f-154">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="bc31f-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="bc31f-155">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bc31f-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-156">**MinEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="bc31f-156">**MinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc31f-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-159">限定詞： **低** ( 「只有從用戶端傳送到伺服器的資料，會根據伺服器的標準索引鍵強度，以加密來保護。</span><span class="sxs-lookup"><span data-stu-id="bc31f-159">Qualifiers: **Low** ("Only data sent from client to server is protected by encryption based on server's standard key strength.</span></span> <span data-ttu-id="bc31f-160">未保護從伺服器傳送到用戶端的資料。」) ， **中型** ( 「伺服器與用戶端之間傳送的所有資料都是根據伺服器的標準索引鍵強度來受到加密保護」。) ， **高** ( 「伺服器與用戶端之間傳送的所有資料都受到以加密為基礎 onserver 的最大金鑰強度」所保護。) </span><span class="sxs-lookup"><span data-stu-id="bc31f-160">Data sent from Server to client is not protected."), **Medium** ("All data sent between Server and client is protected by encryption based on server's standard key strength."), **High** ("All data sent between Server and client is protected by encryption based onserver's maximum key strength.")</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-161">最小加密層級。</span><span class="sxs-lookup"><span data-stu-id="bc31f-161">The minimum encryption level.</span></span>

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="bc31f-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**低** (1) </span><span class="sxs-lookup"><span data-stu-id="bc31f-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-163">低層級的加密。</span><span class="sxs-lookup"><span data-stu-id="bc31f-163">Low level of encryption.</span></span> <span data-ttu-id="bc31f-164">只有從用戶端傳送到伺服器的資料會使用56位加密進行加密。</span><span class="sxs-lookup"><span data-stu-id="bc31f-164">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="bc31f-165">請注意，從伺服器傳送到用戶端的資料並未加密。</span><span class="sxs-lookup"><span data-stu-id="bc31f-165">Be aware that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span data-ttu-id="bc31f-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**中型/用戶端相容** (2) </span><span class="sxs-lookup"><span data-stu-id="bc31f-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Medium / Client Compatible** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-167">用戶端相容的加密層級。</span><span class="sxs-lookup"><span data-stu-id="bc31f-167">Client compatible level of encryption.</span></span> <span data-ttu-id="bc31f-168">從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會以用戶端所支援的最大金鑰強度進行加密。</span><span class="sxs-lookup"><span data-stu-id="bc31f-168">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="bc31f-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**高** (3) </span><span class="sxs-lookup"><span data-stu-id="bc31f-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-170">高層級的加密。</span><span class="sxs-lookup"><span data-stu-id="bc31f-170">High level of encryption.</span></span> <span data-ttu-id="bc31f-171">從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會使用強式128位加密進行加密。</span><span class="sxs-lookup"><span data-stu-id="bc31f-171">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="bc31f-172">無法連接不支援此加密層級的用戶端。</span><span class="sxs-lookup"><span data-stu-id="bc31f-172">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span data-ttu-id="bc31f-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**符合 FIPS 規範** 的 (4) </span><span class="sxs-lookup"><span data-stu-id="bc31f-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**FIPS Compliant** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-174">符合 FIPS 規範的加密。</span><span class="sxs-lookup"><span data-stu-id="bc31f-174">FIPS compliant encryption.</span></span> <span data-ttu-id="bc31f-175">從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會使用 Microsoft 密碼編譯模組，以聯邦資訊處理標準 (FIPS) 加密演算法進行加密和解密。</span><span class="sxs-lookup"><span data-stu-id="bc31f-175">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="bc31f-176">FIPS 是「密碼編譯模組的安全性需求」的標準。</span><span class="sxs-lookup"><span data-stu-id="bc31f-176">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="bc31f-177">FIPS 140-1 (1994) 和 FIPS 140-2 (2001) 描述美國政府內所使用之硬體和軟體密碼編譯模組的政府需求。</span><span class="sxs-lookup"><span data-stu-id="bc31f-177">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc31f-178">**名稱**</span><span class="sxs-lookup"><span data-stu-id="bc31f-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc31f-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-181">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc31f-181">The name of the object.</span></span>

<span data-ttu-id="bc31f-182">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bc31f-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-183">**PolicySourceMinEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="bc31f-183">**PolicySourceMinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-184">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc31f-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-186">指出 **MinEncryptionLevel** 屬性是由伺服器、依群組原則或依預設設定。</span><span class="sxs-lookup"><span data-stu-id="bc31f-186">Indicates whether the **MinEncryptionLevel** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bc31f-187">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="bc31f-187">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-188">伺服器</span><span class="sxs-lookup"><span data-stu-id="bc31f-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-189">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="bc31f-189">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-190">群組原則</span><span class="sxs-lookup"><span data-stu-id="bc31f-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-191">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="bc31f-191">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-192">預設</span><span class="sxs-lookup"><span data-stu-id="bc31f-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc31f-193">**PolicySourceSecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="bc31f-193">**PolicySourceSecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-194">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc31f-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-196">指出 **SecurityLayer** 屬性是由伺服器、依群組原則或依預設設定。</span><span class="sxs-lookup"><span data-stu-id="bc31f-196">Indicates whether the **SecurityLayer** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bc31f-197">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="bc31f-197">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-198">伺服器</span><span class="sxs-lookup"><span data-stu-id="bc31f-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-199">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="bc31f-199">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-200">群組原則</span><span class="sxs-lookup"><span data-stu-id="bc31f-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-201">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="bc31f-201">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-202">預設</span><span class="sxs-lookup"><span data-stu-id="bc31f-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc31f-203">**PolicySourceUserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="bc31f-203">**PolicySourceUserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-204">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc31f-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-206">指出 **UserAuthenticationRequired** 屬性是由伺服器、依群組原則或依預設設定。</span><span class="sxs-lookup"><span data-stu-id="bc31f-206">Indicates whether the **UserAuthenticationRequired** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bc31f-207">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="bc31f-207">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-208">伺服器</span><span class="sxs-lookup"><span data-stu-id="bc31f-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-209">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="bc31f-209">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-210">群組原則</span><span class="sxs-lookup"><span data-stu-id="bc31f-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-211">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="bc31f-211">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-212">預設</span><span class="sxs-lookup"><span data-stu-id="bc31f-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc31f-213">**SecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="bc31f-213">**SecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-214">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc31f-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-216">限定詞： **RDPSecurityLayer** ( "RDP Security Layer： serverand 之間的通訊，用戶端會使用原生 RDP 加密」。) ， **Negotiate** (」將會使用用戶端支援的最安全層。如果支援，則會使用 TLS 1.0。」) ， **ssl** ( SSL (TLS 1.0) 將用於伺服器驗證，以及 forencrypting 伺服器與用戶端之間傳送的所有資料。此設定需要伺服器具有 SSL 相容的憑證。」) ， **NEWTBD** ( 「LONGHORN 中的新安全層」。) </span><span class="sxs-lookup"><span data-stu-id="bc31f-216">Qualifiers: **RDPSecurityLayer** ("RDP Security Layer: Communication between the serverand the client will use native RDP encryption."), **Negotiate** ("The most secure layer that is supported by the client will be used.If supported, TLS 1.0 will be used."), **SSL** ("SSL (TLS 1.0) will be used for server authentication as well as forencrypting all data transferred between the server and the client.This setting requires the server to have an SSL compatible certificate."), **NEWTBD** ("A NEW SECURITY LAYER in LONGHORN.")</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-217">指定用戶端與伺服器之間使用的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="bc31f-217">Specifies the security layer used between the client and server.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="bc31f-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP 安全性層** (1) </span><span class="sxs-lookup"><span data-stu-id="bc31f-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-219">伺服器與用戶端之間的通訊會使用原生 RDP 加密。</span><span class="sxs-lookup"><span data-stu-id="bc31f-219">Communication between the server and the client uses native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="bc31f-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**協商** (2) </span><span class="sxs-lookup"><span data-stu-id="bc31f-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-221">使用用戶端支援的最安全層。</span><span class="sxs-lookup"><span data-stu-id="bc31f-221">The most secure layer that is supported by the client is used.</span></span> <span data-ttu-id="bc31f-222">如果支援，則會使用 SSL (TLS 1.0) 。</span><span class="sxs-lookup"><span data-stu-id="bc31f-222">If supported, SSL (TLS 1.0) is used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="bc31f-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3) </span><span class="sxs-lookup"><span data-stu-id="bc31f-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-224">SSL (TLS 1.0) 用於伺服器驗證，以及加密伺服器與用戶端之間傳送的所有資料。</span><span class="sxs-lookup"><span data-stu-id="bc31f-224">SSL (TLS 1.0) is used for server authentication and for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="bc31f-225">此設定需要伺服器具有 SSL 相容的憑證。</span><span class="sxs-lookup"><span data-stu-id="bc31f-225">This setting requires the server to have an SSL-compatible certificate.</span></span> <span data-ttu-id="bc31f-226">這項設定與 **MinEncryptionLevel** 值1不相容。</span><span class="sxs-lookup"><span data-stu-id="bc31f-226">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span data-ttu-id="bc31f-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4) </span><span class="sxs-lookup"><span data-stu-id="bc31f-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-228">新的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="bc31f-228">A new security layer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc31f-229">**SSLCertificateSHA1Hash**</span><span class="sxs-lookup"><span data-stu-id="bc31f-229">**SSLCertificateSHA1Hash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc31f-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-231">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bc31f-231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-232">以 SSL 憑證的十六進位格式來指定要使用之目標伺服器的 SHA1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="bc31f-232">Specifies the SHA1 hash in hexadecimal format of the SSL certificate for the target server to use.</span></span>

<span data-ttu-id="bc31f-233">您可以使用 [憑證內容] 頁面的 [詳細資料] 索引標籤上的 [憑證] MMC 嵌入式管理單元，找到憑證的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="bc31f-233">The thumbprint of a certificate may be found using the Certificates MMC snap-in on the Details tab of the certificate properties page.</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-234">**SSLCertificateSHA1HashType**</span><span class="sxs-lookup"><span data-stu-id="bc31f-234">**SSLCertificateSHA1HashType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-235">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc31f-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-237">表示 **SSLCertificateSHA1Hash** 屬性的狀態。</span><span class="sxs-lookup"><span data-stu-id="bc31f-237">Indicates the state of the **SSLCertificateSHA1Hash** property.</span></span>

<dt>

<span data-ttu-id="bc31f-238">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="bc31f-238">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-239">無效</span><span class="sxs-lookup"><span data-stu-id="bc31f-239">Not valid</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-240">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="bc31f-240">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-241">預設自我簽署</span><span class="sxs-lookup"><span data-stu-id="bc31f-241">Default self-signed</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-242">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="bc31f-242">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-243">已強制執行預設群組原則</span><span class="sxs-lookup"><span data-stu-id="bc31f-243">Default group policy enforced</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-244">3 (0x3) </span><span class="sxs-lookup"><span data-stu-id="bc31f-244">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="bc31f-245">自訂</span><span class="sxs-lookup"><span data-stu-id="bc31f-245">Custom</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc31f-246">**狀態**</span><span class="sxs-lookup"><span data-stu-id="bc31f-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc31f-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-249">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="bc31f-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-250">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="bc31f-250">Current status of the object.</span></span> <span data-ttu-id="bc31f-251">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="bc31f-251">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="bc31f-252">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="bc31f-252">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="bc31f-253">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="bc31f-253">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bc31f-254">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="bc31f-254">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bc31f-255">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="bc31f-255">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bc31f-256">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bc31f-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="bc31f-257"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="bc31f-257">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bc31f-258"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="bc31f-258">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bc31f-259"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="bc31f-259">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bc31f-260"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="bc31f-260">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bc31f-261"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="bc31f-261">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bc31f-262"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="bc31f-262">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bc31f-263"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="bc31f-263">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bc31f-264"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="bc31f-264">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bc31f-265">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="bc31f-265">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-266">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc31f-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-268">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc31f-268">The name of the terminal.</span></span>

<span data-ttu-id="bc31f-269">這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="bc31f-269">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-270">**TerminalProtocol**</span><span class="sxs-lookup"><span data-stu-id="bc31f-270">**TerminalProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-271">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc31f-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-273">工作階段層通訊協定的名稱;例如，Microsoft RDP 5.0。</span><span class="sxs-lookup"><span data-stu-id="bc31f-273">The name of the session layer protocol; for example, Microsoft RDP 5.0.</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-274">**傳輸**</span><span class="sxs-lookup"><span data-stu-id="bc31f-274">**Transport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-275">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc31f-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-277">連接中使用的傳輸類型;例如，TCP、NetBIOS 或 IPX/SPX。</span><span class="sxs-lookup"><span data-stu-id="bc31f-277">The type of transport used in the connection; for example, TCP, NetBIOS, or IPX/SPX.</span></span>

</dd> <dt>

<span data-ttu-id="bc31f-278">**UserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="bc31f-278">**UserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-279">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc31f-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc31f-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-281">指定用於遠端連線的使用者驗證類型。</span><span class="sxs-lookup"><span data-stu-id="bc31f-281">Specifies the type of user authentication used for remote connections.</span></span> <span data-ttu-id="bc31f-282">如果設定為1，表示已啟用， **UserAuthenticationRequired** 需要在連接時進行使用者驗證，以增加伺服器保護以防止網路攻擊。</span><span class="sxs-lookup"><span data-stu-id="bc31f-282">If set to 1, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="bc31f-283">只有支援 RDP 6.0 版或更高版本的 [遠端桌面通訊協定](remote-desktop-protocol.md) (rdp) 用戶端才能連接。</span><span class="sxs-lookup"><span data-stu-id="bc31f-283">Only [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="bc31f-284">為了避免遠端使用者中斷，建議您在啟用屬性之前，先部署支援適當通訊協定版本的 RDP 用戶端。</span><span class="sxs-lookup"><span data-stu-id="bc31f-284">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

<span data-ttu-id="bc31f-285">您可以使用 [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) 方法來啟用或停用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="bc31f-285">Use the [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) method to enable or disable this property.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bc31f-286"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="bc31f-286"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-287">連接時的使用者驗證已停用。</span><span class="sxs-lookup"><span data-stu-id="bc31f-287">User authentication at connection is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bc31f-288"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="bc31f-288"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-289">在連接時啟用使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="bc31f-289">User authentication at connection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc31f-290">**WindowsAuthentication**</span><span class="sxs-lookup"><span data-stu-id="bc31f-290">**WindowsAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc31f-291">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc31f-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc31f-292">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bc31f-292">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bc31f-293">指定連接是否預設為標準 Windows 驗證程式或已安裝在系統上的另一個驗證套件。</span><span class="sxs-lookup"><span data-stu-id="bc31f-293">Specifies whether the connection defaults to the standard Windows authentication process or to another authentication package that has been installed on the system.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bc31f-294"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="bc31f-294"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-295">不會預設為標準 Windows 驗證進程。</span><span class="sxs-lookup"><span data-stu-id="bc31f-295">Does not default to the standard Windows authentication process.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bc31f-296"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="bc31f-296"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bc31f-297">預設為標準 Windows 驗證進程。</span><span class="sxs-lookup"><span data-stu-id="bc31f-297">Defaults to the standard Windows authentication process.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc31f-298">備註</span><span class="sxs-lookup"><span data-stu-id="bc31f-298">Remarks</span></span>

<span data-ttu-id="bc31f-299">請注意，未與主控台會話相關聯的視窗工作站無法存取此類別的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="bc31f-299">Be aware that window stations not associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="bc31f-300">如果嘗試將 "Console" 指定為 TerminalName 屬性的值，則此物件的方法會傳回 **\_ \_ 不 \_ 支援的 WBEM E**。</span><span class="sxs-lookup"><span data-stu-id="bc31f-300">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="bc31f-301">如果視窗工作站嘗試呼叫此物件的方法，以新增或修改 LocalSystem、LocalService 或 NetworkService 帳戶的安全性屬性，則也會傳回此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bc31f-301">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="bc31f-302">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="bc31f-302">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="bc31f-303">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="bc31f-303">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="bc31f-304">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="bc31f-304">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="bc31f-305">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="bc31f-305">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="bc31f-306">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="bc31f-306">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bc31f-307">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="bc31f-307">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bc31f-308">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="bc31f-308">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bc31f-309">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="bc31f-309">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc31f-310">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc31f-310">Requirements</span></span>



| <span data-ttu-id="bc31f-311">需求</span><span class="sxs-lookup"><span data-stu-id="bc31f-311">Requirement</span></span> | <span data-ttu-id="bc31f-312">值</span><span class="sxs-lookup"><span data-stu-id="bc31f-312">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc31f-313">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc31f-313">Minimum supported client</span></span><br/> | <span data-ttu-id="bc31f-314">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc31f-314">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc31f-315">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc31f-315">Minimum supported server</span></span><br/> | <span data-ttu-id="bc31f-316">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc31f-316">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc31f-317">命名空間</span><span class="sxs-lookup"><span data-stu-id="bc31f-317">Namespace</span></span><br/>                | <span data-ttu-id="bc31f-318">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="bc31f-318">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bc31f-319">MOF</span><span class="sxs-lookup"><span data-stu-id="bc31f-319">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc31f-320"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc31f-320"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc31f-321">DLL</span><span class="sxs-lookup"><span data-stu-id="bc31f-321">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc31f-322"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc31f-322"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc31f-323">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc31f-323">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc31f-324">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="bc31f-324">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 


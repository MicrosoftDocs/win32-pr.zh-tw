---
description: 抓取服務帳戶密碼。
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: 'GetServiceAccountPassword 函式 (Secpkg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: dc00dc01d3acd996257ebc4056be573335a1fd209e9d38abbdcb6bab33124b4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894771"
---
# <a name="getserviceaccountpassword-function"></a>GetServiceAccountPassword 函式

抓取服務帳戶密碼，可供 [*安全性支援提供者*](/windows/desktop/SecGloss/s-gly) (ssp) ，例如 Kerberos SSP。

## <a name="syntax"></a>語法


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AccountName* \[在\]
</dt> <dd>

群組受管理的服務帳戶之以 Null 結束的帳戶名稱 (gMSA) 帳戶。 使用者名稱可以是下列其中一種形式：

-   GMSA 的 SAM 帳戶名稱。
-    (FQDN) 的完整功能變數名稱中的使用者名稱，例如 *DomainName * **\\** _UserName_ 或 **www。**_網域_*_.com \\_ *_名稱_。 使用者名稱必須只有 SAM 名稱。 功能變數名稱可以是 DNS 名稱或 NetBIOS 名稱。
-   GMSA 帳戶的隱含使用者主體名稱 (UPN) ，例如 *SomeName * **@** _Domain_*_.com_*，其中根據隱含 UPN 的定義，*網域 * * * .com** 是實際的網域 DNS 名稱。

</dd> <dt>

*DomainName* \[在中，選擇性\]
</dt> <dd>

選擇性的以 null 終止的功能變數名稱。 只有 *AccountName* 參數是 SAM 帳戶名稱時，此參數才有效。 功能變數名稱只能是 NetBIOS 名稱或完整功能變數名稱 (FQDN) 。

</dd> <dt>

*CredFetch* \[在\]
</dt> <dd>

認證 [**\_ 提取**](cred-fetch.md) 列舉值，指定如何取得認證。



| 值                                                                                                                                                                                                    | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <dt>**CredFetchDefault**</dt> </dl> | 作業系統會先嘗試從本機快取取出密碼（如果不是取得密碼的時候）。 如果需要提取密碼，則作業系統會聯繫網域控制站，否則會傳回狀態為 success 的任何快取密碼。<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <dt>**CredFetchDPAPI**</dt> </dl>         | 將本機 DPAPI 認證傳回給呼叫者。 Ssp 通常不需要使用此值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <dt>**CredFetchForced**</dt> </dl>     | 強制作業系統嘗試從網域控制站讀取密碼。 在密碼變換期間，網域控制站和其他成員主機上的密碼可能已變更，但 gMSA 成員主機會將密碼識別為有效。 這種情況可能是因為不同網域控制站之間的時鐘誤差問題所造成。 指定此值時，作業系統會判斷是否可能因為時鐘誤差而可能變更密碼，如果是，則會抓取密碼。 否則會傳回快取的認證。 如果沒有快取的認證，則作業系統會嘗試從網域控制站取得一個。<br/> |



 

</dd> <dt>

*FileTimeExpiry* \[in、out、optional\]
</dt> <dd>

在輸入時，如果此值為非 null，且不是 **FILETIME**， *FileTimeExpiry* 會包含服務帳戶認證的到期時間（如呼叫端已知）。 如果 *FileTimeExpiry* 參數與目前的其中一個認證相同，則此呼叫會失敗。 在輸出中， *FileTimeExpiry* 參數包含所傳回之認證的到期時間。

</dd> <dt>

*CurrentPassword* \[擴展\]
</dt> <dd>

GMSA 的目前密碼。

</dd> <dt>

*PreviousPassword* \[擴展\]
</dt> <dd>

GMSA 先前的密碼。

</dd> <dt>

*FileTimeCurrPwdValidForOutbound* \[out、optional\]
</dt> <dd>

表示目前的密碼對傳出要求有效的時間。 呼叫端應該將目前的時間與此值進行比較，並使用目前的密碼，只有在目前的時間大於或等於這個參數所傳回的值時才會傳回。 使用這個參數的目的，是針對在輸出邏輯中沒有重試的呼叫端（例如 NTLM）而設計。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「狀態 \_ 成功」。

如果函式失敗，則傳回值為 NTSTATUS 程式碼。 如需詳細資訊，請參閱 [LSA 原則函數傳回值](management-return-values.md)。

您可以使用 [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)函數，將 NTSTATUS 程式碼轉換成 Windows 錯誤碼。

當您完成使用 *CurrentPassword* 和 *PreviousPassword* 參數中所傳回的緩衝區時，請呼叫 [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) 函式釋放它們。

## <a name="remarks"></a>備註

在下列案例中，可以呼叫 **GetServiceAccountPassword** 函數：

-   從安全性支援提供者的登入功能 (SSP) ，SSP 應該會偵測到服務 \_ 帳戶 \_ 密碼用來登入實體，而且應該檢查呼叫端是否具有 TCB 許可權或網路服務。 然後，若要取得最新的認證，SSP 應允許登入程式繼續進行，方法是呼叫 **GetServiceAccountPassword** 函式，並在認證 [**\_ 提取**](cred-fetch.md)列舉中使用 **CredFetchDefault** 值。

-   從 [**InitializeSecurityCoNtext**](../SecAuthN/initializesecuritycontext--general.md) 和 [**AcceptSecurityCoNtext**](../SecAuthN/acceptsecuritycontext--general.md) 呼叫中的 ssp。 Ssp 應該會偵測到服務 \_ 帳戶 \_ 密碼是用於這些呼叫，而如果呼叫是針對非主要認證，則 SSP 應確定呼叫端具有 TCB 許可權或為網路服務。 然後，SSP 應以認證 [**\_ 提取**](cred-fetch.md)列舉中的 **CredFetchDefault** 值呼叫 **GetServiceAccountPassword** 函式，然後繼續進行呼叫。 如果 **InitializeSecurityCoNtext** 和 **AcceptSecurityCoNtext** 呼叫失敗，則 SSP 應使用從上一個呼叫中取出的 FileTimeExpiry，然後 **使用** 該做為輸入，以使用認證 **\_ 提取** 列舉中的 **GetServiceAccountPassword** 值再次呼叫 **CredFetchForced** 。 如果有新的 gMSA 認證可用，則第二次呼叫會成功，並提供新的認證，然後 SSP 應以新的認證重試。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Secpkg。h</dt> </dl> |



 


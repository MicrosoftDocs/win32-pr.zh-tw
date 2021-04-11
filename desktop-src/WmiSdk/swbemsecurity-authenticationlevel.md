---
description: AuthenticationLevel 屬性是一個整數，可定義指派給此物件的 COM 驗證層級。
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: SWbemSecurity. AuthenticationLevel 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 63ae9e529de010e0a0ca7b8bc1da7dc8dc4891b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318860"
---
# <a name="swbemsecurityauthenticationlevel-property"></a>SWbemSecurity. AuthenticationLevel 屬性

**AuthenticationLevel** 屬性是一個整數，可定義指派給此物件的 COM 驗證層級。 此設定會決定您如何保護從 WMI 傳送的資訊。 如需驗證層級的詳細資訊，請參閱 [設定用戶端 \_ 應用程式 \_ 處理安全性](setting-client-application-process-security.md)。 一般情況下，不需要在進行 WMI API 呼叫時設定驗證層級。 如果您未設定此屬性，則會使用系統的預設 COM 驗證層級。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

AuthenticationLevel 設定可讓您要求在整個連接中使用的 DCOM 驗證和隱私權層級。 設定的範圍從無驗證到每個封包加密驗證。



| 值        | 描述                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 無         | 不使用任何驗證。 系統會忽略所有安全性設定。<br/>                                                                                                                                                                                                                                         |
| 預設      | 使用標準安全性協調來選取驗證等級。 這是建議的設定，因為牽涉到交易的用戶端將會與伺服器所指定的驗證層級進行協商。<br/> DCOM 不會在協商會話期間選取 [無] 值。<br/> |
| 連線      | 只有當用戶端嘗試連接到伺服器時，才會驗證用戶端的認證。 建立連線之後，不會進行其他驗證檢查。<br/>                                                                                                                          |
| 呼叫         | 當伺服器收到要求時，只會在每次呼叫的開頭驗證用戶端的認證。 封包標頭已簽署，但在用戶端與伺服器之間交換的資料封包不會進行簽署或加密。<br/>                                                     |
| Pkt          | 驗證從預期的用戶端接收所有資料封包。 類似于呼叫;封包標頭已簽署但未加密。 封包本身不會進行簽署或加密。<br/>                                                                                                               |
| PktIntegrity | 驗證並確認在用戶端與伺服器之間傳輸的資料封包都已修改。 每個資料封包都會經過簽署，以確保在傳輸期間未修改封包。 未加密任何資料封包。<br/>                                            |
| PktPrivacy   | 驗證所有先前的模擬等級，並簽署並加密每個資料封包。 這可確保用戶端與伺服器之間的所有通訊都是機密的。<br/>                                                                                                                             |



 

您可以設定 [**SWbemServices**](swbemservices.md)、 [**SWbemObject**](swbemobject.md)、 [**swbemobjectset 搭配使用**](swbemobjectset.md)、 [**SWbemObjectPath**](swbemobjectpath.md)和 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件的驗證層級，方法是將 **AuthenticationLevel** 屬性設定為所需的值。

下列範例顯示如何設定 **SwbemObject** 物件的驗證層級。


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



您也可以指定驗證層級做為標記的一部分。 下列範例會設定驗證層級和模擬等級，並抓取 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的實例。


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemSecurity<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[設定用戶端 \_ 應用程式 \_ 處理安全性](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> </dl>

 


---
description: ImpersonationLevel 屬性是一個整數，可定義指派給此物件的 COM 模擬層級。
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: SWbemSecurity. ImpersonationLevel 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852627"
---
# <a name="swbemsecurityimpersonationlevel-property"></a>SWbemSecurity. ImpersonationLevel 屬性

**ImpersonationLevel** 屬性是一個整數，可定義指派給此物件的 COM 模擬層級。 這項設定會決定 Windows Management Instrumentation (WMI) 是否可以在呼叫其他進程時偵測或使用您的安全性認證。 如需模擬層級的詳細資訊，請參閱 [設定用戶端 \_ 應用程式 \_ 處理安全性](setting-client-application-process-security.md)。

如果您未明確設定 SWBemSecurity 中的模擬層級，或在安全物件上設定 **ImpersonationLevel** 屬性，則 WMI 會將預設模擬等級設定為 [預設模擬層級](setting-the-default-process-security-level-using-vbscript.md)登錄機碼中指定的值。 如果此設定不足，提供者就不會為您的要求提供服務，而 WMI API 的呼叫可能會失敗，並出現錯誤碼 **wbemErrAccessDenied** (2147749891/0x80041003) 。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

您可以將此屬性設定為下列其中一個值，做為 DCOM 模擬等級：



| 值           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **匿名**   | 隱藏呼叫端的認證。 WMI 實際上不支援此模擬等級;如果腳本指定 impersonationLevel = Anonymous，WMI 將會以無訊息模式升級模擬等級來識別。 不過，這在某些方面是無意義的練習，因為使用識別層級的腳本可能會失敗。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **識別**    | 可讓物件查詢呼叫端的認證。 使用此模擬等級的腳本可能會失敗;識別層級通常可讓您不需要檢查存取控制清單。 您將無法使用 [識別] 對遠端電腦執行腳本。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Impersonate** | 讓物件能夠使用呼叫端的認證。 建議您搭配使用此模擬層級與 WMI 腳本。 當您這樣做時，WMI 腳本會使用您的使用者認證;如此一來，它就能夠執行您可以執行的任何工作。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **代理人**    | 可讓物件允許其他物件使用呼叫端的認證。 委派可讓腳本在遠端電腦上使用您的認證，然後讓該遠端電腦在另一部遠端電腦上使用您的認證。 雖然您可以在 WMI 腳本中使用此模擬層級，但您應該只在必要時才這麼做，因為它可能會造成安全性風險。<br/> 除非交易中所有相關的使用者帳戶和電腦帳戶都已在 Active Directory 中標示為受信任，否則您無法使用委派模擬層級。 這有助於將安全性風險降至最低。 雖然遠端電腦可以使用您的認證，但只有在與交易相關的任何其他電腦都受信任可進行委派時，才可以這樣做。<br/> |



 

如上所述，匿名模擬會隱藏您的認證，並識別允許遠端物件查詢您的認證，但遠端物件無法模擬您的安全性內容。  (換句話說，雖然遠端物件知道您的身分，但它無法「假裝」您 ) 。使用這兩種設定的其中一種來存取遠端電腦的 WMI 腳本通常會失敗。 事實上，大部分的腳本都是在本機電腦上使用這兩種設定的其中一種來執行也會失敗。

模擬允許遠端 WMI 服務使用您的安全性內容來執行要求的作業。 如果您的認證具有足夠的許可權可執行預定的作業，則使用模擬設定的遠端 WMI 要求通常會成功。 換句話說，您不能使用 WMI 來 (遠端執行動作，或者) 您沒有在 WMI 外部執行的許可權。

將 impersonationLevel 設定為 Delegate，可讓遠端 WMI 服務將您的認證傳遞給其他物件，而且通常會被視為安全性風險。

您可以設定 [**SWbemServices**](swbemservices.md)、 [**SWbemObject**](swbemobject.md)、 [**swbemobjectset 搭配使用**](swbemobjectset.md)、 [**SWbemObjectPath**](swbemobjectpath.md)和 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件的模擬層級，方法是將 **ImpersonationLevel** 屬性設定為所需的值。 下列範例說明如何設定 **SWbemObject** 物件的模擬等級：


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



您也可以將模擬層級指定為標記的一部分。 下列範例會設定驗證層級和模擬等級，並抓取 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)的實例。


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
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

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[設定用戶端 \_ 應用程式 \_ 處理安全性](setting-client-application-process-security.md)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 


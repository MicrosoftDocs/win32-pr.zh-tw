---
description: '\_SWbemObject 物件的 security 屬性是用來讀取或設定 SWbemObject 物件的安全性設定。'
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: 'SWbemObject.Security_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d83a155057e445848e727615978c3414e96f63334ffc70c78d5f055a396b53f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313782"
---
# <a name="swbemobjectsecurity_-property"></a>SWbemObject 安全性 \_ 屬性

[**SWbemObject**](swbemobject.md)物件的 **security \_** 屬性是用來讀取或設定 **SWbemObject** 物件的安全性設定。 這個屬性是 [**SWbemSecurity**](swbemsecurity.md) 物件。 此物件中的安全性設定不會指出對 Windows Management Instrumentation (WMI) 的連線所進行的驗證、模擬或許可權設定，或是當物件在非同步呼叫中傳遞到接收時，對 proxy 的安全性有效。 如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。

> [!Note]  
> 將 [**SWbemObject**](swbemobject.md)物件的 [**安全性 \_** ] 屬性設定為 **Null** ，會將無限存取權授與所有人。 如需詳細資訊，請參閱 [**SWbemSecurity**](swbemsecurity.md)。

 

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a>屬性值

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)
</dt> <dt>

[設定用戶端 \_ 應用程式 \_ 處理安全性](setting-client-application-process-security.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**許可權常數**](privilege-constants.md)
</dt> </dl>

 

 





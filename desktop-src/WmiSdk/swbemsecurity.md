---
description: SWbemSecurity 物件會取得或設定指派給物件的安全性設定，例如許可權、COM 模擬和驗證層級。
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: 'SWbemSecurity 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978874"
---
# <a name="swbemsecurity-object"></a>SWbemSecurity 物件

**SWbemSecurity** 物件會取得或設定指派給物件的安全性設定，例如許可權、COM 模擬和驗證層級。 [**Wbemscripting.swbemlocator**](swbemlocator.md)、 [**SWbemServices**](swbemservices.md)、 [**SWbemObject**](swbemobject.md)、 [**swbemobjectset 搭配使用**](swbemobjectset.md)、 [**SWbemObjectPath**](swbemobjectpath.md)、 [**SWbemLastError**](swbemlasterror.md)和 [**SWbemEventSource**](swbemeventsource.md)物件都有 **安全性 \_** 屬性，也就是 **SWbemSecurity** 物件。 當您取得實例或查看 WMI 安全性記錄檔時，可能需要設定 **安全性 \_** 物件的屬性。

VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫無法建立安全性物件。 此物件中的安全性設定不會識別 WMI 連線上的驗證、模擬或許可權設定，或在非同步呼叫中將物件傳遞到接收時，對 proxy 的安全性有效。 如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。

## <a name="members"></a>成員

**SWbemSecurity** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SWbemSecurity** 物件具有這些屬性。



| 屬性                                                                    | 存取類型           | Description                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)<br/> | 讀取/寫入<br/> | 數值，定義指派給這個物件的 COM 驗證層級。 此設定會決定您如何保護從 WMI 傳送的資訊。<br/>                                                                 |
| [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)<br/>   | 讀取/寫入<br/> | 數值，定義指派給這個物件的 COM 模擬層級。 這項設定會決定 WMI 所擁有的進程是否可以在呼叫其他進程時，偵測或使用您的安全性認證。<br/> |
| [**特權**](swbemsecurity-privileges.md)<br/>                   | 唯讀<br/>  | [**SWbemPrivilegeSet**](swbemprivilegeset.md)物件，定義此物件的許可權。 如需詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。<br/>                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemSecurity<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> <dt>

[設定用戶端 \_ 應用程式 \_ 處理安全性](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 


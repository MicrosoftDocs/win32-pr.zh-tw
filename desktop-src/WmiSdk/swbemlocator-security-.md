---
description: '\_Wbemscripting.swbemlocator 物件的 security 屬性是用來讀取或設定 wbemscripting.swbemlocator 物件的安全性設定。 這個屬性是 SWbemSecurity 物件。'
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: 'SWbemLocator.Security_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6c5fa2ba102de1135c0019e2dcfb291f55672cabb00cea1c59d8a655f21c882e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955168"
---
# <a name="swbemlocatorsecurity_-property"></a>Wbemscripting.swbemlocator 安全性 \_ 屬性

[**Wbemscripting.swbemlocator**](swbemlocator.md)物件的 **security \_** 屬性是用來讀取或設定 **wbemscripting.swbemlocator** 物件的安全性設定。 這個屬性是 [**SWbemSecurity**](swbemsecurity.md) 物件。

> [!Note]  
> 將 [**wbemscripting.swbemlocator**](swbemlocator.md)物件的 [**安全性 \_** ] 屬性設定為 **Null** ，會將無限存取權授與所有人。 如需詳細資訊，請參閱 [**SWbemSecurity**](swbemsecurity.md)。

 

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

**Wbemscripting.swbemlocator 安全性 \_** 物件的屬性沒有預設值。 如果您在設定 [**wbemscripting.swbemlocator**](swbemlocator.md)物件之前嘗試取得 [**SWbemSecurity. AuthenticationLevel**](swbemsecurity-authenticationlevel.md)或 [**SWbemSecurity**](swbemsecurity-impersonationlevel.md)的值，就會產生 [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)錯誤結果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ wbemscripting.swbemlocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Wbemscripting.swbemlocator**](swbemlocator.md)
</dt> <dt>

[建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)
</dt> <dt>

[使用 VBScript 執行特殊許可權作業](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[設定用戶端 \_ 應用程式 \_ 處理安全性](setting-client-application-process-security.md)
</dt> <dt>

[**SWbemSecurity 物件**](swbemsecurity.md)
</dt> <dt>

[保護遠端 WMI 連接](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 





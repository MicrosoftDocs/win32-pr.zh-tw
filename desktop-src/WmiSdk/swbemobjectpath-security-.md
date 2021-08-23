---
description: SWbemObjectPath 物件的 Security 屬性是用來取得或設定物件路徑的安全性元件。
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: 'SWbemObjectPath.Security_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ed473049de6973da077b1ccfabdd3fe752ff4e5edd13f4a49a7c5589309ae81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639968"
---
# <a name="swbemobjectpathsecurity_-property"></a>SWbemObjectPath 安全性 \_ 屬性

[**SWbemObjectPath**](swbemobjectpath.md)物件的 **security** 屬性是用來取得或設定物件路徑的安全性元件。 請注意，它不會用來設定 **SWbemObjectPath** 物件本身的安全性屬性。 它只能用來代表 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件的路徑安全性元件。 這個屬性是 [**SWbemSecurity**](swbemsecurity.md) 物件。

> [!Note]  
> 將 [**SWbemObjectPath**](swbemobjectset.md)物件的 [[**安全性 \_**](swbemobject-security-.md) ] 屬性設定為 **Null** ，會將無限存取權授與所有人。 如需詳細資訊，請參閱 [**SWbemSecurity**](swbemsecurity.md)。

 

如需詳細資訊，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemObjectPath.Security_ As Object
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
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> <dt>

[建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)
</dt> <dt>

[設定用戶端 \_ 應用程式 \_ 處理安全性](setting-client-application-process-security.md)
</dt> </dl>

 

 





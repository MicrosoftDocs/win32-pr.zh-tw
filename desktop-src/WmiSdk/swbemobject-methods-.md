---
description: '\_SWbemObject 物件的方法屬性會傳回 SWbemMethodSet 物件，該物件為目前類別或實例的方法集合。 這是唯讀的屬性。'
ms.assetid: ef9abced-5126-4698-b01e-f3e9c871162f
ms.tgt_platform: multiple
title: 'SWbemObject.Methods_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Methods_
- ISWbemObject.Methods_
- ISWbemObject.get_Methods_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e0442798a7630de20ff062a631baa335c5f6ed960900d571ca1d0e9e9a067f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991978"
---
# <a name="swbemobjectmethods_-property"></a>SWbemObject 方法 \_ 屬性

[**SWbemObject**](swbemobject.md)物件的 **方法 \_** 屬性會傳回 [**SWbemMethodSet**](swbemmethodset.md)物件，該物件為目前類別或實例的方法集合。 這是唯讀的屬性。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemObject.Methods_ As Object
```



## <a name="property-value"></a>屬性值

## <a name="examples"></a>範例

下列程式 [代碼範例](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1)（取自 TechNet 資源庫）說明如何列出類別的所有方法。


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Methods" 
WScript.Echo "---------------------------" 
  
For Each objClassMethod In objClass.Methods_ 
    WScript.Echo objClassMethod.Name 
Next 
```



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



 

 





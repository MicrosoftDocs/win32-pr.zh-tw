---
description: 設定或取得布林值，這個值會指定是否可以使用使用者介面提示輸入簽署者或寄件者的身分識別。
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: EnablePromptForCertificateUI 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990673"
---
# <a name="settingsenablepromptforcertificateui-property"></a>EnablePromptForCertificateUI 屬性

\[**EnablePromptForCertificateUI** 屬性可用於 [需求] 區段中指定的作業系統。\]

**EnablePromptForCertificateUI** 屬性會設定或取得布林值，這個值會指定是否可以使用使用者介面提示輸入簽署者或寄件者的身分識別。

## <a name="syntax"></a>Syntax


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 true**，則可使用使用者介面提示輸入簽署者或寄件者的身分識別。 預設值為 **false**。

> [!Note]  
> 設定這個屬性並不會停用從 web 應用程式完成任何私密金鑰使用之前所產生的警告。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**設定**](settings.md)
</dt> </dl>

 

 





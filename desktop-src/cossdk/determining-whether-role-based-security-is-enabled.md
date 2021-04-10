---
description: 判斷是否已啟用 Role-Based 安全性
ms.assetid: b5e6ab7e-5a77-4c6f-9bec-02942bba389d
title: 判斷是否已啟用 Role-Based 安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ccf6f95b9c8776a45c071f6d4ea3326eda035c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111436"
---
# <a name="determining-whether-role-based-security-is-enabled"></a>判斷是否已啟用 Role-Based 安全性

藉由使用安全性呼叫內容物件中提供的 [**ISecurityCallCoNtext：： IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) 方法，您可以判斷目前物件是否已啟用安全性。 您應在使用 ISecurityCallCoNtext：：[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)檢查角色成員資格之前呼叫 **IsSecurityEnabled** ，因為如果未啟用安全性， **IsCallerInRole** 會傳回 True。

Microsoft Visual Basic 開發人員呼叫 [**GetSecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) 來取得 [**SecurityCallCoNtext**](securitycallcontext.md) 物件的參考，然後呼叫 [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled)，如下列範例所示：


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



Microsoft Visual C++ 開發人員可以呼叫 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)來呼叫 [**ISecurityCallCoNtext：： IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) ，以取得 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)的指標，然後呼叫 **IsSecurityEnabled**。 以下是一個簡單的範例：


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsEnabled;

HRESULT hr1 = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr1)) throw(hr1);
if (NULL == pSecCtx) {
    // Display error message.
    return E_FAIL;
}

HRESULT hr2 = pSecCtx->IsSecurityEnabled(&bIsEnabled);
return hr2;
```



雖然呼叫 [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) 的慣用方式是使用安全性呼叫內容物件，您也可以透過物件內容來呼叫 **IsSecurityEnabled** 。 如需詳細資訊， (查看 [**ObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) 或 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) 。 ) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[存取安全性呼叫內容資訊](accessing-security-call-context-information.md)
</dt> <dt>

[檢查角色成員資格](checking-role-membership.md)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> </dl>

 

 

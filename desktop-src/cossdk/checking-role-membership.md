---
description: 檢查角色成員資格
ms.assetid: 690cab3f-4476-4fce-b842-d63a4d0d5c6f
title: 檢查角色成員資格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 777d47b36d2eea79d8b16e7025839b696c38ff87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689012"
---
# <a name="checking-role-membership"></a>檢查角色成員資格

您可以呼叫 [**ISecurityCallCoNtext：： IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) 方法，判斷物件的直接呼叫端是否為特定角色的成員。 如果您想要確保特定的程式碼區塊不會執行，除非呼叫端是特定角色的成員，這項功能就很有用。

例如，您可以使用 [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) 來確保超過指定金額的交易（例如 $1000）只由管理員角色的成員執行。 如果呼叫端不是管理員，而且交易超過 $1000，則不會執行交易，且會顯示錯誤訊息。

存取 [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) 的慣用方法是透過安全性呼叫內容物件，因為您可以使用安全性呼叫內容物件的相同參考來取得安全性屬性。 不過，您也可以從 **ObjectCoNtext** 物件存取 **IsCallerInRole** 方法。 如需詳細資訊， (查看 [**ObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) 或 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) 。 ) 

如果您正在開發 Microsoft Visual Basic 應用程式的元件，請呼叫 [**GetSecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) 函式，然後使用安全性呼叫內容來呼叫 [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)，如下列範例所示：


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



如果您正在開發 C 或 c + + 應用程式，請使用 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) 來取出 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) 介面的指標。 然後您會呼叫 [**ISecurityCallCoNtext：： IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)，如下列範例所示：


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsInRole;

HRESULT hr = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr)) throw(hr);
if (NULL == pSecCtx) { 
    // No security call context is available.
    // Display an error message and return.
    return E_FAIL;
}
hr = pSecCtx->IsCallerInRole(myRole, &bIsInRole);
return hr;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[存取安全性呼叫內容資訊](accessing-security-call-context-information.md)
</dt> <dt>

[判斷是否已啟用 Role-Based 安全性](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> </dl>

 

 

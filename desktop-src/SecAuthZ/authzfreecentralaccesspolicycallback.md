---
description: AuthzFreeCentralAccessPolicyCallback 函式是應用程式定義的函式，可釋出由 AuthzGetCentralAccessPolicyCallback 函數配置的記憶體。
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: AuthzFreeCentralAccessPolicyCallback 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195578"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a>AuthzFreeCentralAccessPolicyCallback 回呼函式

*AuthzFreeCentralAccessPolicyCallback* 函式是應用程式定義的函式，可釋出由 [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md)函數配置的記憶體。 *AuthzFreeCentralAccessPolicyCallback* 是應用程式定義函數名稱的預留位置。

## <a name="syntax"></a>語法


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCentralAccessPolicy* \[在\]
</dt> <dd>

要釋放的集中存取原則指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回 **TRUE**。

如果函數無法執行評估，則會傳回 **FALSE**。 使用 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) 將錯誤傳回存取檢查函數。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AUTHZ \_ INIT \_ 資訊**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 

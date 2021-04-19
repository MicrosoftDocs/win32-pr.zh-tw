---
description: AuthzGetCentralAccessPolicyCallback 函式是可取得集中存取原則的應用程式定義函數。 AuthzGetCentralAccessPolicyCallback 是應用程式定義函數名稱的預留位置。
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: AuthzGetCentralAccessPolicyCallback 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976376"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a>AuthzGetCentralAccessPolicyCallback 回呼函式

*AuthzGetCentralAccessPolicyCallback* 函式是可取得集中存取原則的應用程式定義函數。 *AuthzGetCentralAccessPolicyCallback* 是應用程式定義函數名稱的預留位置。

## <a name="syntax"></a>語法


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hAuthzClientCoNtext* \[在\]
</dt> <dd>

用戶端內容的控制碼。

</dd> <dt>

*capid* \[在\]
</dt> <dd>

要取出的集中存取原則識別碼。

</dd> <dt>

*pArgs* \[在中，選擇性\]
</dt> <dd>

透過 [**AUTHZ \_ 存取 \_ 要求**](/windows/desktop/api/Authz/ns-authz-authz_access_request)結構的 **OptionalArguments** 成員傳遞至 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)函數的選擇性引數。

</dd> <dt>

*pCentralAccessPolicyApplicable* \[擴展\]
</dt> <dd>

指向布林值的指標，資源管理員會使用這個值指出是否應該在存取評估期間使用集中存取原則。

</dd> <dt>

*ppCentralAccessPolicy* \[擴展\]
</dt> <dd>

用來評估存取權的集中存取原則 (端點) 的指標。 如果這個值為 **Null**，則會套用預設上限。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回 **TRUE**。

如果函數無法執行評估，則會傳回 **FALSE**。 使用 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) 將錯誤傳回存取檢查函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                   |
| 可轉散發套件<br/>          | Windows XP 上的 windows Server 2003 管理工具套件<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AUTHZ \_ 存取 \_ 要求**](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[**AUTHZ \_ INIT \_ 資訊**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 


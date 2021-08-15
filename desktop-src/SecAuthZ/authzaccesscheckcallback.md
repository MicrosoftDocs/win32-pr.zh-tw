---
description: 應用程式定義的函式，可處理在存取檢查期間)  (Ace 的回呼存取控制專案。
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: AuthzAccessCheckCallback 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5079b740d268174715b6c944787bb687cd9b8b1ecb12a27c04eeb26c79811034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784154"
---
# <a name="authzaccesscheckcallback-callback-function"></a>AuthzAccessCheckCallback 回呼函式

**AuthzAccessCheckCallback** 函式是一種應用程式定義函式，可處理存取檢查期間)  (ace 的回呼 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)。 **AuthzAccessCheckCallback** 是應用程式定義函數名稱的預留位置。 應用程式會藉由呼叫 [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)來註冊此回呼。

## <a name="syntax"></a>語法


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hAuthzClientCoNtext* \[在\]
</dt> <dd>

用戶端內容的控制碼。

</dd> <dt>

*步調* \[在\]
</dt> <dd>

要在呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) 函式時，所要評估的 ACE 指標。

</dd> <dt>

*pArgs* \[在中，選擇性\]
</dt> <dd>

在呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)或 [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)的 *DynamicGroupArgs* 參數中傳遞的資料。

</dd> <dt>

*pbAceApplicable* \[in、out\]
</dt> <dd>

布林值變數的指標，此變數會接收應用程式所定義之邏輯的評估結果。

如果邏輯判斷 ACE 適用且將包含在 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)的呼叫中，則結果為 **TRUE** 。否則，結果為 **FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回 **TRUE**。

如果函數無法執行評估，則會傳回 **FALSE**。 使用 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) 將錯誤傳回存取檢查函數。

## <a name="remarks"></a>備註

如果在條件運算式中參考，則安全性屬性變數必須存在於用戶端內容中，否則參考它們的條件運算式詞彙將會評估為 unknown。

如需詳細資訊，請參閱 [AccessCheck 的運作方式](how-dacls-control-access-to-an-object.md) 和 [集中式授權原則](centralized-authorization-policy.md) 的總覽。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                   |
| 可轉散發套件<br/>          | WindowsWindows XP 上的 Server 2003 管理工具套件<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[基本存取控制功能](authorization-functions.md)
</dt> <dt>

[集中式授權原則](centralized-authorization-policy.md)
</dt> <dt>

[AccessCheck 的運作方式](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 


---
description: 應用程式定義的函式，會建立套用至用戶端 (Sid) 的安全識別碼清單。 AuthzComputeGroupsCallback 是應用程式定義函數名稱的預留位置。
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: AuthzComputeGroupsCallback 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7c30194e4131cbd375192723e23308e1ad5ead69d849ab73857f72ef1d4b0790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784076"
---
# <a name="authzcomputegroupscallback-callback-function"></a>AuthzComputeGroupsCallback 回呼函式

**AuthzComputeGroupsCallback** 函式是一種應用程式定義的函式，它會建立適用于用戶端 (sid) 的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly)清單。 **AuthzComputeGroupsCallback** 是應用程式定義函數名稱的預留位置。

## <a name="syntax"></a>語法


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hAuthzClientCoNtext* \[在\]
</dt> <dd>

用戶端內容的控制碼。

</dd> <dt>

*Args* \[在\]
</dt> <dd>

在呼叫 [**AuthzInitializeCoNtextFromAuthzCoNtext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)、 [**AuthzInitializeCoNtextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)或 [**AuthzInitializeCoNtextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)函數的 *DynamicGroupArgs* 參數中傳遞的資料。

</dd> <dt>

*pSidAttrArray* \[擴展\]
</dt> <dd>

指標變數的指標，此變數會接收 [**SID \_ 和 \_ 屬性**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) 結構陣列的位址。 這些結構代表用戶端所屬的群組。

</dd> <dt>

*pSidCount* \[擴展\]
</dt> <dd>

*PSidAttrArray* 中的結構數目。

</dd> <dt>

*pRestrictedSidAttrArray* \[擴展\]
</dt> <dd>

指標變數的指標，此變數會接收 [**SID \_ 和 \_ 屬性**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) 結構陣列的位址。 這些結構代表受限於用戶端的群組。

</dd> <dt>

*pRestrictedSidCount* \[擴展\]
</dt> <dd>

*PSidRestrictedAttrArray* 中的結構數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功傳回 Sid 清單，則傳回值為 **TRUE**。

如果函式失敗，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

應用程式也可以藉由呼叫 [**AuthzAddSidsToCoNtext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)，將 sid 新增至用戶端內容。

使用邏輯運算子時，屬性變數的格式必須是運算式;否則會評估為 unknown。

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

[**AuthzAddSidsToCoNtext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthzInitializeCoNtextFromAuthzCoNtext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[**AuthzInitializeCoNtextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[**AuthzInitializeCoNtextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[**SID \_ 和 \_ 屬性**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 


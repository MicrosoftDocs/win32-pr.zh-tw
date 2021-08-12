---
description: 提供安全性資訊集合的存取，代表呼叫者的身分識別。 使用這個類別，您可以在屬於安全性呼叫內容一部分的呼叫端中找出特定的呼叫端。
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: 'SecurityIdentity 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: d16139ccf60a22ebfb4cf609e734e0b8df3285ef9ddb1804657313900a3ea05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305474"
---
# <a name="securityidentity-class"></a>SecurityIdentity 類別

提供安全性資訊集合的存取，代表呼叫者的身分識別。 使用這個類別，您可以在屬於安全性呼叫內容一部分的呼叫端中找出特定的呼叫端。 如需如何存取安全性呼叫內容資訊的詳細資訊，請參閱程式設計元件安全性。

只有使用以角色為基礎之安全性的 COM + 應用程式才能存取 **SecurityIdentity** 類別。 如需角色的詳細資訊，請參閱以 [角色為基礎的安全性管理](role-based-security-administration.md)。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|--------------------------------------------------------|
| 介面 | [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a>使用時機

您可以使用這個類別來存取 [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)的方法。

## <a name="remarks"></a>備註

您無法直接建立 **SecurityIdentity** 物件。 若要使用 [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)的方法，您必須藉由呼叫 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)（ \_ 為 *riid* 參數提供 IID ISecurityCallCoNtext）來取得其實址的參考。 接下來，呼叫 [**ISecurityCallCoNtext：： get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) ，要求 (安全性識別集合的安全性呼叫內容專案，例如 "DirectCaller" 或 "OriginalCaller" ) 。 然後呼叫 [**ISecurityIdentityColl：： get \_ 專案**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) 以抓取 (的安全性識別專案，例如 "Name" 或 "AuthenticationService" ) 。

若要從 Microsoft Visual Basic 使用這個類別，請新增 com + 服務類型程式庫的參考。 您無法直接建立 SecurityIdentity 物件。 若要使用其屬性，您必須使用 [**GetSecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)來取得其執行的參考。 接下來，取得物件的 Item 屬性，要求安全性識別集合 (的安全性呼叫內容專案，例如 "DirectCaller" 或 "OriginalCaller" ) 。 然後，使用 SecurityIdentity 物件的 Item 屬性來取出安全性識別專案 (例如 "Name" 或 "AuthenticationService" ) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>ComSvcs。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetSecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> <dt>

[以角色為基礎的安全性管理](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallCoNtext**](securitycallcontext.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> </dl>

 


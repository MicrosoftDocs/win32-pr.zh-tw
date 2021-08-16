---
description: 提供呼叫端集合中個別呼叫端的相關資訊。 集合代表以目前呼叫結尾的呼叫鏈，而集合中的每個呼叫端都代表一個呼叫端的身分識別。
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: 'SecurityCallers 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: a494e1421e443d2a6c3663bd7fa7c15eda898079477592e8df9958a2d5b87990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915892"
---
# <a name="securitycallers-class"></a>SecurityCallers 類別

提供呼叫端集合中個別呼叫端的相關資訊。 集合代表以目前呼叫結尾的呼叫鏈，而集合中的每個呼叫端都代表一個呼叫端的身分識別。 只有跨越已檢查安全性之界限的呼叫端才會包含在呼叫端鏈中。  (在 COM + 環境中，系統會在應用程式界限檢查安全性。您可以透過 [**SecurityIdentity**](securityidentity.md) 類別（身分識別集合）提供有關特定呼叫端身分識別的資訊 ) 存取。

只有使用以角色為基礎之安全性的 COM + 應用程式才能存取 **SecurityCallers** 類別。 如需角色的詳細資訊，請參閱以 [角色為基礎的安全性管理](role-based-security-administration.md)。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|------------------------------------------------------|
| 介面 | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>使用時機

您可以使用這個類別來存取 [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)的方法。

## <a name="remarks"></a>備註

您無法直接建立 **SecurityCallers** 物件。 若要使用 [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)的方法，您必須藉由呼叫 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)（ \_ 為 *riid* 參數提供 IID ISecurityCallCoNtext）來取得其實址的參考。 接下來，呼叫 [**ISecurityCallCoNtext：： get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) ，要求 (安全性識別集合的安全性呼叫內容專案，例如 "DirectCaller" 或 "OriginalCaller" ) 。

若要從 Microsoft Visual Basic 使用這個類別，請新增 com + 服務類型程式庫的參考。 您無法直接建立 SecurityCallers 物件。 若要使用其屬性，您必須使用 [**GetSecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)來取得其執行的參考。 接下來，取得物件的 Item 屬性，要求安全性識別集合 (的安全性呼叫內容專案，例如 "DirectCaller" 或 "OriginalCaller" ) 。

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

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 


---
description: 提供存取目前呼叫的安全性內容，其中包含物件呼叫端的相關資訊。
ms.assetid: e8ac05fb-6665-4e57-b64e-82d9799d29d4
title: 'SecurityCallCoNtext 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallContext
api_type:
- COM
ms.openlocfilehash: bd15b7e0317a507a2340cc148bb927bb5d94a37b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106998962"
---
# <a name="securitycallcontext-class"></a>SecurityCallCoNtext 類別

提供存取目前呼叫的安全性內容，其中包含物件呼叫端的相關資訊。 您也可以使用這個類別，找出物件的直接呼叫端是否為特定角色的成員，以及物件是否啟用安全性。

只有使用以角色為基礎之安全性的 COM + 應用程式才能存取 **SecurityCallCoNtext** 類別。 如需角色的詳細資訊，請參閱以 [角色為基礎的安全性管理](role-based-security-administration.md)。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|------------------------------------------------------|
| 介面 | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>使用時機

您可以使用這個類別來存取 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)的方法。

## <a name="remarks"></a>備註

您無法直接建立 **SecurityCallCoNtext** 物件。 若要使用 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)的方法，您必須藉由呼叫 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)（ \_ 為 *riid* 參數提供 IID ISecurityCallCoNtext）來取得其實址的參考。

若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。 您可以使用 "COMSVCSLib. SecurityCallCoNtext" 將 SecurityCallCoNtext 物件宣告為類別名稱;它是透過呼叫 [**GetSecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)來建立。

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

[**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> <dt>

[以角色為基礎的安全性管理](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> <dt>

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 


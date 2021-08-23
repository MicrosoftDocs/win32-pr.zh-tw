---
title: External. accountType
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 AccountType 屬性會抓取目前使用者的帳戶類型。
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- Windows Media Player 的外部 accountType
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bd19413d891f5a8008b162f6795af29a9d15e75a80d35bb82ff13f8e013da9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650038"
---
# <a name="externalaccounttype"></a>External. accountType

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**AccountType** 屬性會抓取目前使用者的帳戶類型。

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a>可能的值

這個屬性是代表帳戶類型的唯讀 **字串** 。 代表不同帳戶類型的字串是由線上商店所定義。

## <a name="remarks"></a>備註

這個屬性會藉由呼叫 [IWMPContentPartner：： GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) 方法（由線上商店的外掛程式所執行）來抓取帳戶類型。 如果目前的使用者已登入線上商店，或外掛程式已快取使用者的認證，則 **getContentPartnerInfo** 方法可以判斷使用者的帳戶類型，並將其傳回 Windows Media Player。 帳戶類型是 Windows Media Player 不會解讀的字串。 相反地，Windows Media Player 會將來自線上商店之外掛程式的字串傳遞至線上商店的 [探索] 頁面上的腳本。

如果目前的使用者未登入線上商店，且線上商店的外掛程式沒有使用者的快取認證，則此屬性會在該情況下抓取 **getContentPartnerInfo** 方法所傳回的任何字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**UserLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 






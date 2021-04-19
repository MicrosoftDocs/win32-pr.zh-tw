---
title: External. 驗證方法
description: 驗證方法會起始驗證使用者的嘗試。
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- 驗證方法 Windows Media Player
- 驗證方法 Windows Media Player、外部類別
- 外部類別 Windows Media Player，驗證方法
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977531"
---
# <a name="externalauthenticate-method"></a>External. 驗證方法

**驗證** 方法會起始驗證使用者的嘗試。

## <a name="syntax"></a>語法


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*AuthenticationIndex* \[在\]
</dt> <dd>

指定驗證-成功網頁索引的 (**long**) **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

[探索] 頁面上的某些連結具有應只在使用者經過驗證之後才顯示的目標。 [探索] 頁面、Windows Media Player 和線上商店的外掛程式會使用下列步驟來驗證使用者，並顯示目標網頁：

1.  探索頁面上的腳本會呼叫 *External*。**驗證** 方法。
2.  Windows Media Player 會顯示一個對話方塊，以取得使用者名稱和密碼。
3.  Windows Media Player 會呼叫 [IWMPContentPartner：：](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate)authentication，此動作會起始驗證嘗試，並立即傳回。
4.  當驗證嘗試完成時，線上商店的外掛程式會呼叫 [IWMPContentPartnerCallback：： Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)，傳遞 wmpcnAuthResult 和指出嘗試是否成功的布林值。
5.  如果驗證嘗試成功，Windows Media Player 會呼叫 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)，傳遞 g \_ szItemInfo \_ AuthenticationSuccessURL，以取得驗證成功網頁的 URL。 在此呼叫中，Windows Media Player 會傳遞探索頁面傳遞給 *外部* 的相同索引。**驗證** 方法。
6.  Windows Media Player 顯示驗證-成功網頁。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**AttemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**UserLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 






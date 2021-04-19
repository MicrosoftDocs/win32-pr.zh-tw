---
title: explicit_handle 屬性
description: '\ Explicit \_ 控制碼 \ ACF 屬性指定每個程式都有一個基本控制碼，例如控制碼 t 型別，做為第一個參數 \_ 。'
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965202"
---
# <a name="explicit_handle-attribute"></a>明確 \_ 控制碼屬性

\[**明確的 \_ 控制碼** \] ACF 屬性指定每個程式都有一個基本控制碼，例如 [**控制碼 \_ t 型別**](handle-t.md)，做為第一個參數。

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

當您使用 **\[ 明確 \_ 控制碼 \]** 屬性時，每個程式都有一個基本控制碼做為第一個參數，即使 IDL 檔案未在其參數清單中包含這個控制碼也是一樣。 發出至標頭檔和存根常式的原型包含額外的參數，並使用該參數做為導向遠端呼叫的控制碼。

**\[ 明確的 \_ 句 \] 柄** 屬性會同時影響遠端程式和序列化程式。 針對型別序列化，會使用初始參數做為明確 (序列化) 控制碼來產生支援常式。 如果未使用 **\[ 明確的 \_ 句 \] 柄** 屬性，應用程式仍然可以指定作業具有明確的控制碼 (系結或序列化) 導向呼叫。 若要這樣做，具有包含控制碼類型之引數的原型會提供給 IDL 檔案。 請注意，在預設模式下，未先出現的引數也可以做為控制碼來導向呼叫。

因此，雖然 **\[ 明確的 \_ 句 \] 柄** 屬性是一種提供 idl 原型的基本 **\[ 明確 \_ 控制碼 \]** 屬性的方式，但不一定需要變更 IDL 檔案。 在 [**/osf**](-osf.md) 模式中，只有第一個引數可以當做明確的控制碼類型使用。

**\[ 明確 \_ 控制碼 \]** 屬性可以當做介面屬性或作業屬性使用。 作為介面屬性，它會影響介面中的所有作業，以及需要序列化支援的所有類型。 但是，如果使用它做為作業屬性，它只會影響該特定的作業。 如果方法 \[ 在內容控制碼中包含一或多個 \] ，則 \[ 會使用最左邊的 \] 內容控制碼作為系結控制碼，而不會建立其他明確的控制碼。

## <a name="examples"></a>範例

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**自動 \_ 處理**](auto-handle.md)
</dt> <dt>

[**隱含 \_ 控制碼**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 





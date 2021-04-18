---
title: force_allocate 屬性
description: ACF 屬性 \ force \_ 配置 \ 強制使用 midl 使用者配置來配置指標參數， \_ \_ 而不是將配置優化。
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate 屬性 MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463008"
---
# <a name="force_allocate-attribute"></a>強制 \_ 配置屬性

ACF 屬性 \[ **強制 \_ 配置** \] 會強制使用 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md)來配置指標參數，而不是將配置優化。

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>參數

這個屬性沒有任何參數。

## <a name="remarks"></a>備註

RPC 會藉由提供內部記憶體緩衝區的指標，嘗試將伺服器上的記憶體配置降至最低。 這種方法可能會導致應用程式發生問題，而這些應用程式嘗試在 RPC 提供的指標上直接呼叫 [**midl \_ 使用者 \_**](midl-user-free-1.md) ，因為已優化的指標無法釋放。 使用 **\[ 強制 \_ 配置 \]** 來標記參數，將會使所有衍生它的指標都無法進行優化。

**\[ 強制 \_ 配置 \]** 的另一種常見用法，是在應用程式需要大於所指向記憶體的對齊情況時，保證所指向的記憶體對齊。 例如，應用程式通常會以位元組的泛型陣列來傳遞資料，而不是使用實際的型別，但是位元組只保證會對齊1，這可能會對採用較大對齊的應用程式造成問題。 藉由使用 **\[ 強制 \_ 配置 \]** 來標記參數，應用程式可以保證所指向的所有記憶體都具有等於 [**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md)所保證的對齊。

## <a name="examples"></a>範例

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[避免資訊隱藏](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[設計64位相容介面](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[**midl \_ 使用者 \_ 配置**](midl-user-allocate-1.md)
</dt> <dt>

[**midl \_ 使用者 \_ 免費**](midl-user-free-1.md)
</dt> <dt>

[**分配**](allocate.md)
</dt> </dl>

 

 
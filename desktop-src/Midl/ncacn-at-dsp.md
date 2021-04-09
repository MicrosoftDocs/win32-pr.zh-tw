---
title: ncacn_at_dsp 屬性
description: Ncacn \_ at \_ dsp 關鍵字會將 AppleTalk dsp 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933201"
---
# <a name="ncacn_at_dsp-attribute"></a>ncacn \_ 于 \_ dsp 屬性

**Ncacn \_ at \_ dsp** 關鍵字會將 AppleTalk dsp 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a>參數

<dl> <dt>

*埠名稱* 
</dt> <dd>

指定長度最多為22個位元組的字元字串。

</dd> </dl>

## <a name="remarks"></a>備註

AppleTalk DSP 埠字串的語法（如同所有的埠字串）是由傳輸執行所定義，而且與 IDL 規格無關。 MIDL 編譯器會執行有限的語法檢查，但不保證端點規格是正確的。 某些錯誤類別可能會在執行時間（而不是在編譯時期）回報。

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**端點**](endpoint.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**字串系結**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 
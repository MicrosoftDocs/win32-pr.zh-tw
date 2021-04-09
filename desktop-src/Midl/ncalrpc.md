---
title: ncalrpc 屬性
description: Ncalrpc 關鍵字會將本機處理序間通訊識別為端點的通訊協定系列。 這個關鍵字是必須搭配 \ endpoint \ 屬性使用的其中一個有效通訊協定系列名稱。
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- ncalrpc 屬性 MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f20ae9e347303288868eeb16758736047fecc1b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933205"
---
# <a name="ncalrpc-attribute"></a>ncalrpc 屬性

**Ncalrpc** 關鍵字會將本機處理序間通訊識別為端點的通訊協定系列。 此關鍵字是必須搭配端點屬性使用的其中一個有效的通訊協定系列名稱 **\[** [](endpoint.md) **\]** 。

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a>參數

<dl> <dt>

*埠名稱* 
</dt> <dd>

指定通訊埠的字元字串， (應用程式、服務或) 服務的實例，以供用戶端用來對伺服器進行進程間呼叫。 字串最多可以包含53個字元，而且不能包含任何反斜線 (\) 字元。 電腦名稱稱不得與 **ncalrpc** 關鍵字一起使用。

</dd> </dl>

## <a name="remarks"></a>備註

本機處理序間通訊埠字串的語法（如同所有的埠字串）是由傳輸執行所定義，而且與 IDL 規格無關。 MIDL 編譯器會執行有限的語法檢查，但不保證端點規格是正確的。 某些錯誤類別可能會在執行時間（而不是在編譯時期）回報。

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
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

[**\_在 \_ dsp ncacn**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ nsp**](ncacn-dnet-nsp.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ ipx**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[字串系結](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 
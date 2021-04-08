---
title: /oldnames 參數
description: /Oldnames 參數會指示 MIDL 編譯器產生不包含版本號碼的介面名稱。
ms.assetid: 3a79c399-e115-46fd-9559-681b85cd872d
keywords:
- /oldnames 參數 MIDL
topic_type:
- apiref
api_name:
- /oldnames
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cf861d2bf4f4123d7a1ee103e6966e5d404946
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681894"
---
# <a name="oldnames-switch"></a>/oldnames 參數

**/Oldnames** 參數會指示 MIDL 編譯器產生不包含版本號碼的介面名稱。

``` syntax
midl /oldnames
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

MIDL 編譯器會將介面的版本號碼併入存根中產生的介面名稱 (例如，iface \_ v1 \_ 0 \_ ServerIfHandle) 。 此命名格式與憑證 DCE IDL 編譯器所使用的格式一致。 但是，它與 MIDL 1.0 編譯器所使用的命名格式不同。 MIDL 1.0 編譯器不包含介面名稱中的版本號碼 (例如 iface \_ ServerIfHandle) 。 **/Oldnames** 參數可讓您指示 MIDL 編譯器產生不包含版本號碼的介面名稱。 如此一來，格式會與 MIDL 1.0 編譯器所產生的名稱一致。

如果您的伺服器應用程式程式碼是以 MIDL 1.0 編譯器產生的存根來使用，而它是指 MIDL 產生的介面名稱 (例如，在 [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)) 的呼叫中，您應該將它變更為參考 midl 編譯器2.0 版或更新版本所支援的介面名稱樣式。 或者，您可以在叫用 MIDL 編譯器時使用 **/oldnames** 參數。

## <a name="examples"></a>範例

**midl/oldnames 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> </dl>

 

 
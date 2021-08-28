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
ms.openlocfilehash: 9b7906878c7ba10681cbf361a4671370331fbcb5abee73eb212dcac4ab41443d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992028"
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

 

 
---
title: /use_epv 參數
description: /Use \_ epv 參數會指示 MIDL 編譯器產生伺服器 stub 程式碼，該程式碼會透過進入點向量 (epv) ，而不是透過靜態呼叫來呼叫伺服器應用程式常式。 不建議使用此屬性。
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv switch MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966446"
---
# <a name="use_epv-switch"></a>/use \_ epv 參數

**/Use \_ epv** 參數會指示 MIDL 編譯器產生伺服器 stub 程式碼，該程式碼會透過進入點向量 (epv) ，而不是透過靜態呼叫來呼叫伺服器應用程式常式。 不建議使用此屬性。

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

一般而言，應用程式需要將靜態連結到伺服器應用程式常式。 MIDL 編譯器預設會產生這類呼叫。 但是，如果應用程式需要伺服器 stub 才能使用 epv 來呼叫伺服器應用程式常式，就必須指定 **/use \_ epv** 參數。 當指定 **/use \_ epv** 參數時，MIDL 編譯器會產生預設 epv。 如果應用程式未透過 [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) 呼叫註冊另一個 epv，則會使用此預設 epv。

## <a name="examples"></a>範例

**midl/use \_ epv** *檔案名 * * * .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**/no \_ 預設 \_ epv**](-no-default-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 
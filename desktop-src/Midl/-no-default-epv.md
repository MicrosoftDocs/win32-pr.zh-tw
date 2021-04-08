---
title: /no_default_epv 參數
description: /No \_ 預設 \_ epv 參數會指示 MIDL 編譯器不要產生預設的進入點向量 (epv) 。 不建議使用此屬性。
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv switch MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933127"
---
# <a name="no_default_epv-switch"></a>/no \_ 預設 \_ epv 參數

**/No \_ 預設 \_ epv** 參數會指示 MIDL 編譯器不要產生預設的進入點向量 (epv) 。 不建議使用此屬性。

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

在此情況下，應用程式必須向 [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) 呼叫註冊 epv。 將此參數與 [**/use \_ epv**](-use-epv.md) 參數進行比較。

## <a name="examples"></a>範例

**midl/no \_ 預設 \_ epv 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**/use \_ epv**](-use-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 
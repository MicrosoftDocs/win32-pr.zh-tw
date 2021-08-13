---
title: /rpcss 參數
description: 指定/rpcss 參數時，會將 \_ 介面的所有作業都指定為啟用配置屬性。 不建議使用此屬性。
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- /rpcss 參數 MIDL
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0c3087f47bd12c852ef168b2684d5b094239cdac45933c8e7d831fc6461c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643738"
---
# <a name="rpcss-switch"></a>/rpcss 參數

指定 **/rpcss** 參數時，會將介面的所有作業都指定為 [**啟用 \_ 配置**](enable-allocate.md) 屬性。 不建議使用此屬性。

``` syntax
midl /rpcss
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

在預設模式下，只有在程式或介面具有 [**啟用 \_ 配置**](enable-allocate.md) 屬性，或在命令列上指定 **/rpcss** 參數時，才會啟用 RpcSs 套件。 在 **/osf** 模式中，伺服器端 stub 會啟用 RpcSs 配置封裝。

## <a name="examples"></a>範例

**midl/rpcss 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**啟用 \_ 配置**](enable-allocate.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 





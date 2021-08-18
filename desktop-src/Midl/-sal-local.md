---
title: /sal_local 參數
description: /Sal \_ 本機參數會將 MIDL 導向至另一個標記為 \ local \ 之介面方法參數的 sal 注釋。 /Sal 參數也必須存在。
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local switch MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666401cca482846fc2e6a9d5851a4da9d2d362279c9bc1496ab672a94ac9b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014086"
---
# <a name="sal_local-switch"></a>/sal \_ 本機參數

**/Sal \_ 本機** 參數會指示 MIDL 針對標記為 [**\[ \] local**](local.md)之介面方法的參數產生 sal 注釋。 [**/Sal**](-sal.md)參數也必須存在。

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

修改 [**/sal**](-sal.md)參數的行為，也會提供標記有 [**\[ 區域 \]**](local.md)屬性之介面方法參數的附注。 使用 [ [**\[ 批註 \]**](annotate.md)] 屬性可使用不同的批註字串來覆寫 MIDL 產生的注釋。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**\[注釋\]**](annotate.md)
</dt> </dl>

 

 





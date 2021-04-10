---
title: /msc_ver 參數
description: /Msc \_ ver 參數是用來允許 MIDL 產生程式碼，其中包含不同版本的 Microsoft C/c + + 編譯器的優化。
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver switch MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841428"
---
# <a name="msc_ver-switch"></a>/msc \_ ver 參數

**/Msc \_ ver** 參數是用來允許 MIDL 產生程式碼，其中包含不同版本的 Microsoft C/c + + 編譯器的優化。

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*版本 \_ 號碼* 
</dt> <dd>

指定將用來編譯分散式應用程式之用戶端和伺服器存根的 Microsoft Visual C++ 編譯器的整數版本號碼。 預設版本號碼是1100，對應至 Visual C++ 版本5.0。 版本號碼1200對應于 Visual C++ 版本6.0，依此類推。

</dd> </dl>

## <a name="remarks"></a>備註

特別是，1100或更高版本的版本值會導致 MIDL 編譯器使用 **\_ \_ declspec (uuid () )** 指示詞來產生程式碼。 它也會啟用使用 **\_ \_ declspec (selectany)** 和 **\_ \_ declspec (novtable)** 指示詞的宏。

 

 





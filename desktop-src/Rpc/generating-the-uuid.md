---
title: 產生 UUID
description: 定義介面的第一個步驟是使用 uuidgen.exe 公用程式來產生 (UUID) 的通用唯一識別碼。
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- 遠端程序呼叫 RPC、工作、產生 UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e263bfe21c4a564106c0d6328c0de891c18bca1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839951"
---
# <a name="generating-the-uuid"></a>產生 UUID

定義介面的第一個步驟是使用 **uuidgen.exe** 公用程式來產生 (UUID) 的通用唯一識別碼。 UUID 可讓用戶端和伺服器應用程式彼此識別。 當您安裝平臺軟體發展工具組 (SDK) 時，會自動安裝 **uuidgen.exe** 公用程式 (Uuidgen.exe) 。

下列命令會產生 UUID，並建立名為 Hello 的範本檔案。

**uuidgen.exe/i/ohello.idl**

當然，您的 hello .idl 範本看起來會像這樣 (使用不同的 UUID) 。

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 





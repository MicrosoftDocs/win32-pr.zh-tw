---
title: 固定陣列
description: 如果您的介面指定具有特定元素數目的陣列做為參數，則會使用固定陣列。 使用 MIDL 時，您會以 C 中定義的相同方式定義固定陣列。您可以指定陣列的類型、名稱和大小。
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1040e417cc896b9f4bd2271dc69e23033332354357b2aad32053724d94b79035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929977"
---
# <a name="fixed-arrays"></a>固定陣列

如果您的介面指定具有特定元素數目的陣列做為參數，則會使用固定陣列。 使用 MIDL 時，您會以 C 中定義的相同方式定義固定陣列。您可以指定陣列的類型、名稱和大小。

下列範例示範如何定義固定陣列。

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

當用戶端程式將固定陣列傳遞至伺服器程式時，用戶端存根會將整個陣列傳送至伺服器 stub。 伺服器 stub 會為數組配置記憶體，並將其在網路上收到的陣列資料儲存至配置的記憶體中。 然後，它會將陣列傳遞至伺服器上的遠端程式。 伺服器可能會修改陣列中的資料。

當遠端程式終止時，伺服器存根會將陣列的內容傳送回用戶端。 用戶端存根會將它從伺服器 stub 收到的資料複製到原始陣列中。 然後，用戶端程式就可以使用資料，就像從本機程序呼叫接收資料一樣。

 

 





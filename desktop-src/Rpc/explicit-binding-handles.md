---
title: 明確的系結控制碼
description: 為了充分掌控系結程式，用戶端/伺服器應用程式可能會使用明確的系結控制碼。
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a6e723d8559dc5e72783412eb6250f69431f31d08a92c4984fb2e2a19b761d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930017"
---
# <a name="explicit-binding-handles"></a>明確的系結控制碼

為了充分掌控系結程式，用戶端/伺服器應用程式可能會使用明確的系結控制碼。 和隱含的控制碼一樣，明確的系結控制碼可讓您的用戶端應用程式選取伺服器來執行其呼叫。 此外，明確的系結控制碼可讓您的用戶端/伺服器應用程式建立已驗證的 RPC 通訊會話。 使用明確的控制碼時，您的用戶端可以連接到多部伺服器，並在多部伺服器上執行遠端程式。 多執行緒和非同步用戶端應用程式甚至可以連接至多部伺服器，並同時執行多個遠端程式。

您的用戶端應用程式必須將明確控制碼作為參數傳遞給每個遠端程序呼叫。 為了符合憑證標準，應將控制碼指定為每個遠端程式上的第一個參數。 不過，Microsoft 的 RPC 擴充功能可讓您指定其他位置的系結控制碼。 如需詳細資訊，請參閱 [MICROSOFT RPC Binding-Handle 擴充](microsoft-rpc-binding-handle-extensions.md)功能。

若要建立明確的控制碼，請將控制碼宣告為 IDL 檔案中遠端作業的參數。 您可以重新定義 [Hello，World 範例](tutorial.md) 以使用明確的控制碼，如下所示：

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

您可以在單一介面中結合明確和隱含控制碼。 如果函式在其參數清單中有明確的控制碼，則會使用該控制碼。 如果使用隱含控制碼之介面中的函式未指定明確的控制碼，則會使用預設的隱含控制碼。

 

 





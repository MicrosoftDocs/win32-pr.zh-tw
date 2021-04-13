---
title: 用戶端存根
description: 用戶端 stub 模組會針對輸入 IDL 檔案中定義的每個作業，在用戶端上提供代理的進入點。
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL 和 RPC MIDL、介面、用戶端 stub
- 介面 MIDL
- 介面 MIDL、MIDL 和 RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301567"
---
# <a name="the-client-stub"></a>用戶端存根

用戶端 stub 模組會針對輸入 IDL 檔案中定義的每個作業，在用戶端上提供代理的進入點。

當用戶端應用程式呼叫遠端程式時，其呼叫會先進入用戶端 stub 檔案中的代理常式。 用戶端 stub 常式會執行下列功能：

-   封送處理引數。 用戶端存根會將輸入引數封裝到可傳送至伺服器的表單中。
-   呼叫用戶端執行時間程式庫，將引數傳送至遠端位址空間，並叫用伺服器位址空間中的遠端程式。
-   拆收輸出引數。 用戶端存根解壓縮輸出引數，並傳回給呼叫端。

MIDL 編譯器會將 [**/client**](-client.md)、 [**/cstub**](-cstub.md)和 [**/out**](-out.md) 參數切換至用戶端存根檔案。

 

 





---
title: 伺服器 Stub
description: 伺服器 stub 會針對輸入 IDL 檔案中定義的每個作業，在伺服器上提供代理的進入點。
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL 編譯器 MIDL、MIDL 和 RPC MIDL、介面、伺服器 stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021882"
---
# <a name="the-server-stub"></a>伺服器 Stub

伺服器 stub 會針對輸入 IDL 檔案中定義的每個作業，在伺服器上提供代理的進入點。

當 RPC 執行時間程式庫叫用伺服器 stub 常式時，它會執行下列功能：

-   拆收輸入引數 (從) 的傳輸格式中解壓縮引數。
-   呼叫伺服器上程式的實際執行。
-   封送處理輸出引數 (將引數封裝到傳送的表單) 。

MIDL 編譯器會將 [**/server**](-server.md)、 [**/sstub**](-sstub.md)和 [**/out**](-out.md) 切換為伺服器存根檔案。

 

 





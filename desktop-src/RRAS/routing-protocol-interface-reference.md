---
title: 路由通訊協定介面參考
description: 本檔說明用來將路由通訊協定實作為使用者模式 DLL 的函式和結構。
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- 路由及遠端存取服務 RRAS，路由通訊協定介面，參考
- 路由通訊協定介面 RRAS，參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0196a5cbad8919a07a6e9a19ee5f7848eb6378ad2c56f7f0977125e5e79133a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027348"
---
# <a name="routing-protocol-interface-reference"></a>路由通訊協定介面參考

本檔說明用來將路由通訊協定實作為使用者模式 DLL 的函式和結構。

MPR50 應該在路由通訊協定的 make 檔案中定義。

**SIZEOF ip 系結 \_ \_ (x)** 宏會計算 ip 配接器系結 [**\_ \_ \_ 資訊**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info)結構的大小（以位元組為單位），其中包含 ip 位址的數目。

下列主題將描述這些參考元素：

-   [路由通訊協定介面函式](routing-protocol-interface-functions.md)
-   [路由通訊協定介面結構](routing-protocol-interface-structures.md)
-   [IPX 服務資料表管理](ipx-service-table-management.md)

 

 





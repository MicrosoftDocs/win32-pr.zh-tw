---
title: RPC 緩衝區配置錯誤
description: 因為 RPC 執行時間程式庫會為傳送和接收緩衝區配置記憶體，所以函式應該會預期 RPC 配置錯誤。
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe48c113d644447b5ff7b69988f2534d7de3a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300804"
---
# <a name="rpc-buffer-allocation-errors"></a>RPC 緩衝區配置錯誤

因為 RPC 執行時間程式庫會為傳送和接收緩衝區配置記憶體，所以函式應該會預期 RPC 配置錯誤。 發生 RPC 配置錯誤時，可繼續的控制碼會失效。 這是一項需求，因為無法 rewindable 可繼續的函式。

 

 





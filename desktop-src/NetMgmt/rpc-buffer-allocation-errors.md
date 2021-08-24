---
title: RPC 緩衝區配置錯誤
description: 因為 RPC 執行時間程式庫會為傳送和接收緩衝區配置記憶體，所以函式應該會預期 RPC 配置錯誤。
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c484837f1f03bce8a8175ddb343065051e3695eec7c65d8a9de89c15fb5d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745008"
---
# <a name="rpc-buffer-allocation-errors"></a>RPC 緩衝區配置錯誤

因為 RPC 執行時間程式庫會為傳送和接收緩衝區配置記憶體，所以函式應該會預期 RPC 配置錯誤。 發生 RPC 配置錯誤時，可繼續的控制碼會失效。 這是一項需求，因為無法 rewindable 可繼續的函式。

 

 





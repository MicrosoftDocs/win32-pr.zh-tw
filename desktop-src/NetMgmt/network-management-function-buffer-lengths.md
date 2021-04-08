---
title: 網路管理函數緩衝區長度
description: 本主題討論與網路管理 Api 搭配使用時的函式緩衝區長度需求。
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840116"
---
# <a name="network-management-function-buffer-lengths"></a>網路管理函數緩衝區長度

本主題討論與網路管理 Api 搭配使用時的函式緩衝區長度需求。

在呼叫網路管理列舉函式 (和各種資料抓取函式時，指定緩衝區大小的應用程式) 必須指定夠大的緩衝區來保存傳回的資訊結構 (或結構) 加上其成員指向的字串。 如果您沒有指定夠大的緩衝區來接收所有可用的專案，函數會傳回錯誤的 \_ \_ 資料。 列舉呼叫不會傳回部分專案。

某些網路管理函式會採用諮詢最大的資料長度參數 *prefmaxlen*。 此參數可讓應用程式建議伺服器從函式呼叫傳回的位元組數目。

如果您 \_ 在 prefmaxlen 參數中指定 [最大慣用長度] 值 \_ ，網路管理函數會配置資料所需的記憶體數量。 

如需詳細資訊，請參閱 [網路管理函數緩衝區](network-management-function-buffers.md)。

 

 





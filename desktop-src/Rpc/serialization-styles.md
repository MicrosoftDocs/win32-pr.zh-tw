---
title: 序列化樣式
description: 您可以使用三種樣式來操作序列化控制碼。
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfaa7cd3198245441a27990d331bcd9f0bd0396b5075d9985b13da58012147d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925384"
---
# <a name="serialization-styles"></a>序列化樣式

您可以使用三種樣式來操作序列化控制碼。 這些警告是：

-   [固定緩衝區序列化](fixed-buffer-serialization.md)
-   [動態緩衝區序列化](dynamic-buffer-serialization.md)
-   [累加式序列化](incremental-serialization.md)

無論您使用何種樣式，都必須建立序列化控制碼、序列化資料，然後釋放控制碼。 當程式建立控制碼並定義緩衝區操作的方式時，就會設定樣式。 控制碼會維護與三個序列化樣式相關聯的適當內容。

 

 





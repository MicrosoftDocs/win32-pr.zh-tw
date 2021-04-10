---
title: 內嵌字串
description: 資訊結構將不會包含內嵌字串。 這可改善資訊結構的對齊，並允許在核心功能中提供 OEM 彈性。
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673919"
---
# <a name="embedded-strings"></a>內嵌字串

資訊結構將不會包含內嵌字串。 這可改善資訊結構的對齊，並允許在核心功能中提供 OEM 彈性。

列舉呼叫中所傳回的任何資訊欄位，都可以用來做為呼叫 GetInfo 網路管理函式的索引鍵，以保證存在於列舉緩衝區中。 如果指定索引鍵域值的可變長度資訊字串無法容納，則不會傳回專案的整個固定長度結構。 其他可變長度的欄位將會以 **Null** 指標傳回，表示字串不符合的情況。

 

 





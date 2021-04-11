---
description: 您可以更新 union view 類別實例的非索引鍵屬性值。 您對 view 類別實例所做的變更將會傳播回組成 union view 類別的來源類別實例。
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: 更新聯集視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114844"
---
# <a name="updating-a-union-view"></a>更新聯集視圖

您可以更新 union view 類別實例的非索引鍵屬性值。 您對 view 類別實例所做的變更將會傳播回組成 union view 類別的來源類別實例。

下列限制適用于 view 類別實例的變更：

-   您無法建立 view 類別的新實例。
-   只有 union 類別支援更新;聯結和相關檢視會建立唯讀的視圖實例。
-   更新成功與否取決於來源實例是否可更新。 如果視圖實例屬性對應至來源實例的唯讀屬性，則嘗試修改 view 屬性將會失敗。

 

 




---
description: PublishProduct 動作會使用系統來管理產品資訊的公告。 如果產品處於公告模式或正在安裝或重新安裝任何功能，則此動作會發佈產品。
ms.assetid: aba1baf2-d282-4f76-87aa-67188b779535
title: PublishProduct 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9edf95ccb736bb4a4388f36d87bfbfbe299573e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996719"
---
# <a name="publishproduct-action"></a>PublishProduct 動作

PublishProduct 動作會使用系統來管理產品資訊的公告。 如果產品處於公告模式或正在安裝或重新安裝任何功能，則此動作會發佈產品。

## <a name="sequence-restrictions"></a>順序限制

PublishProduct 動作必須晚于 [PublishFeatures](publishfeatures-action.md) 動作。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述        |
|-------|-----------------------------------|
| \[1\] | 已公告產品的識別碼。 |



 

 

 




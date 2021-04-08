---
title: 複合檔案優化
description: 非同步存放裝置可讓應用程式精確配置複合檔案，讓資料可依應用程式的要求順序提供。
ms.assetid: 0737c5b2-09f6-4993-bb42-f2a684e5a136
keywords:
- 複合檔案優化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb55d4d9ba7b264c1a0aac4252d879a7ba98b6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671667"
---
# <a name="compound-file-optimization"></a>複合檔案優化

非同步存放裝置可讓應用程式精確配置複合檔案，讓資料可依應用程式的要求順序提供。 如果應用程式只需要部分資料來顯示第一頁的資訊，則可以將此資料放在檔案的開頭，即使它邏輯上位於資料流程的結尾。 來自不同資料流程的資料可以交錯。 例如，音訊和影片資料可以交錯，讓後續的讀取作業同時抓取，這是多媒體應用程式的需求。

[**IStorage：： CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) 可以用來配置 e，藉此改善大部分案例的效能。

 

 





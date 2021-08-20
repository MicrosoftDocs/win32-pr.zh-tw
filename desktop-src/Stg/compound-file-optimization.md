---
title: 複合檔案優化
description: 非同步存放裝置可讓應用程式精確配置複合檔案，讓資料可依應用程式的要求順序提供。
ms.assetid: 0737c5b2-09f6-4993-bb42-f2a684e5a136
keywords:
- 複合檔案優化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc98265cc25908459a256f96dd992ba9177364451164e6ec41519363a171943c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962418"
---
# <a name="compound-file-optimization"></a>複合檔案優化

非同步存放裝置可讓應用程式精確配置複合檔案，讓資料可依應用程式的要求順序提供。 如果應用程式只需要部分資料來顯示第一頁的資訊，則可以將此資料放在檔案的開頭，即使它邏輯上位於資料流程的結尾。 來自不同資料流程的資料可以交錯。 例如，音訊和影片資料可以交錯，讓後續的讀取作業同時抓取，這是多媒體應用程式的需求。

[**IStorage：： CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) 可以用來配置 e，藉此改善大部分案例的效能。

 

 





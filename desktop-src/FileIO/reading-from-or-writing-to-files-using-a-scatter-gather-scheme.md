---
description: 描述在一項作業中用來讀取或寫入非連續資料區塊的散佈集合配置。
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: 使用 Scatter-Gather 配置讀取或寫入檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc8a7ee9fcae2a54ac31c51a7c038e3d9442a6ccded2fc7dab916c7a6165a68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914478"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>使用 Scatter-Gather 配置讀取或寫入檔案

散佈收集配置會使用作業系統，在一個作業中傳遞多個離散的資料區塊 (例如，從檔案) 的資料庫記錄，到記憶體中的非連續緩衝區。 散佈式收集配置也會在一項作業中從非連續的緩衝區寫入資料。

應用程式可以使用 [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) 和 [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) 函式來執行散佈集合配置。

 

 




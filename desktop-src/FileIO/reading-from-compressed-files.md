---
description: 應用程式可以使用 LZSeek 和 LZRead 函數，一次將壓縮檔案解壓縮。
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: 從壓縮檔案讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984642"
---
# <a name="reading-from-compressed-files"></a>從壓縮檔案讀取

除了在單一作業中解壓縮完整的檔案之外，應用程式也可以使用 [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) 和 [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) 函式，一次將壓縮檔案解壓縮到一個部分。 當需要解壓縮大型檔案的元件時，這些函數特別有用。 例如，除了字元資料以外，字型製造商可能會有包含字型度量的壓縮檔案。 若要使用這些檔案中的資訊，應用程式必須解壓縮檔案;不過，大部分的應用程式在任何特定時間都只會使用部分檔案。 為了取得字型計量的相關資訊，應用程式會從標頭中提取資料。 若要從文字取得資訊，應用程式會藉由呼叫 **LZSeek** 並藉由呼叫 **LZRead** 來解壓縮字元資料，來重新放置檔案指標的位置。

 

 




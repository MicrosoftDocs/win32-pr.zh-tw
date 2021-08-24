---
title: 判斷驅動程式是否可以處理輸入格式
description: 判斷驅動程式是否可以處理輸入格式
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，輸入格式
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，輸入格式
- ICDrawQuery 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1453348c52ed8244ac81f830299a632f2fbe9cab03461303d9aa841dcd675666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497288"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a>判斷驅動程式是否可以處理輸入格式

下列範例顯示如何使用 [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) 宏來檢查輸入格式。


```C++
// lpbiIn points to BITMAPINFOHEADER structure indicating the input 
// format. 

if (ICDrawQuery(hIC, lpbiIn) == ICERR_OK) 
{ 
    // Driver recognizes the input format. 
} 
else 
{ 
    // Need a different decompressor. 
} 
 
```



 

 





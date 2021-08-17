---
title: 建立物件指標
description: 建立物件指標
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586ba0b8c9ee261e29f21ed58c84193f4cc89d1399c62d75d82a2c0a49075dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144681"
---
# <a name="creating-an-object-pointer"></a>建立物件指標

AVIBall 會使用下列結構作為其物件指標。 此結構的第一個成員指向 AVIBall 用來存取其函數的虛擬函式資料表。 應用程式可以將此結構轉換成 PAVISTREAM 資料類型。 使用 PAVISTREAM 資料類型的方法只會使用虛擬函式資料表的指標。 AVIBall 會在內部使用虛擬函式資料表指標後面的成員。


```C++
typedef struct 
{ 
    IAVIStreamVtbl FAR * lpvtbl; 
 
    // Ball instance data. 
    ULONG     ulRefCount; 
    DWORD     fccType;  // is this audio/video? 
    int        width;    // size, in pixels, of each frame 
    int        height; 
    int        length;   // length, in frames 
    int        size; 
    COLORREF    color;    // ball color 
} AVIBALL, FAR * PAVIBALL; 

```



 

 





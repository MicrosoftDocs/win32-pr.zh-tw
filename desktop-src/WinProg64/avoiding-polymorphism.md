---
title: 避免多型
description: 新的資料類型包括兩個多型類型： INT \_ PTR 和 LONG \_ PTR。
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- 多型64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf107c64f0f4d7e1c0127337401f8dcf057d2ef7b7281455df361da3c519065
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928015"
---
# <a name="avoiding-polymorphism"></a>避免多型

新的資料類型包括兩個多型類型： **INT \_ PTR** 和 **LONG \_ PTR**。 在32位 Windows 上， **int \_ ptr** 會對應到 **int** ，而 **long \_ ptr** 會對應至 **long**。 在64位 Windows 上，這兩種類型都會對應至 **\_ \_ int64** 內建類型。 MIDL 編譯器支援這些類型進行遠端程序呼叫，但在分散式環境中使用這些類型時，您必須記住這項固有的限制。 請務必適當地批註您的程式碼。

無論平臺大小為何，這些多型類型的網路大小一律為32位。 在64位 Windows 上進行封送時，執行時間程式庫符號會擴充帶正負號的值，並將零指派給不帶正負號值的高序位位元組。 將64位值放在網路上時，執行時間會截斷高序位的位元組。 因此，只有低序位的32位值可以使用。

只有在移植需要時，才使用多型類型。 針對新的介面，請使用 MIDL 內建整數類型 **\_ \_ int32** 和 **\_ \_ int64**，或使用指標類型或內容控制碼，以最適合傳送的資料類型為准。

64位編譯器支援新的多型內建函式內部 **\_ \_ int3264**。 同樣地，這種類型是為了支援移植工作而開發的，在此情況下，可透明地支援 **UINT \_ PTR** 類型。  (另一個內建 **\_ \_ long3264**，將會 **支援 \_ ULONG PTR** 類型。 ) 不會直接使用 **\_ \_ int3264** ; 當您基於移植原因需要多型型別時，請使用 **INT \_ ptr** 型別。

 

 





---
title: 累加式序列化
description: 當使用累加樣式序列化時，您會提供三個常式來操作緩衝區。
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf559e94b4476d5dfabdfbb8f040ce8323bc202f4111e9eae95aa257f8e2b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929046"
---
# <a name="incremental-serialization"></a>累加式序列化

當使用累加樣式序列化時，您會提供三個常式來操作緩衝區。 這些常式包括：配置、讀取和寫入。 配置常式會配置所需大小的緩衝區。 寫入常式會將資料寫入緩衝區，而讀取常式會抓取包含已封送資料的緩衝區。 單一序列化呼叫可以對這些常式進行數個呼叫。

序列化的遞增樣式使用下列常式：

-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

您必須提供之配置、讀取和寫入函式的原型如下所示：

``` syntax
void __RPC_USER Alloc (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returns pointer to allocated buffer */
   unsigned int *pSize); /* inputs requested bytes; outputs 
                         /* pBuffer size */

void __RPC_USER Write (
   void *State,          /* application-defined pointer */
   char *Buffer,         /* buffer with serialized data */
   unsigned int Size);   /* number of bytes to write from Buffer */

void __RPC_USER Read (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returned pointer to buffer with data */
   unsigned int *pSize); /* number of bytes to read into pBuffer */
```

所有三個函式的狀態輸入參數都是與編碼服務控制碼相關聯的應用程式定義指標。 應用程式可以使用這個指標來存取包含應用程式特定資訊的結構，例如，檔案控制代碼或資料流程指標。 請注意，除了傳遞給配置、讀取和寫入函式以外，存根不會修改狀態指標。 在編碼期間，會呼叫配置以取得資料已序列化的緩衝區。 然後，會呼叫 Write 來讓應用程式控制序列化資料的儲存時間和位置。 在解碼期間，會呼叫 Read 來傳回所要求的序列化資料位元組數目，從應用程式儲存的位置。

累加樣式的一項重要功能是，控制碼會為您保持狀態指標。 除了將指標傳遞至配置、寫入或讀取函式時，此指標會維持狀態，而且 RPC 函式永遠不會觸及這些函數。 此控制碼也會維護內部狀態，讓您可以視需要新增填補來將數個型別實例編碼和解碼成相同的緩衝區。 [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)函式會將控制碼重設為其初始狀態，以啟用從緩衝區開頭讀取或寫入的功能。

配置和寫入函式，以及應用程式定義的指標，會透過呼叫 [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) 函式與編碼服務控制碼相關聯。 **MesEncodeIncrementalHandleCreate** 會配置控制碼所需的記憶體，然後將它初始化。

應用程式可以呼叫 [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) 來建立解碼控制碼、 [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) 重新初始化控制碼，或使用 [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) 來釋放控制碼的記憶體。 Read 函式和應用程式定義的參數，會透過呼叫 **MesDecodeIncrementalHandleCreate** 常式來與解碼控制碼相關聯。 函式會建立控制碼，並將其初始化。

[**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)的 UserState、配置、寫入和讀取參數可以是 **Null** ，表示沒有任何變更。

 

 





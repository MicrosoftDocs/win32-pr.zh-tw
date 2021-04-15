---
title: 動態緩衝區序列化
description: 使用動態緩衝區的序列化樣式時，會由存根配置封送處理緩衝區，並將資料編碼到這個緩衝區，並傳回給您。 當您進行封送時，您會提供包含資料的緩衝區。
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462216"
---
# <a name="dynamic-buffer-serialization"></a>動態緩衝區序列化

使用動態緩衝區的序列化樣式時，會由存根配置封送處理緩衝區，並將資料編碼到這個緩衝區，並傳回給您。 當您進行封送時，您會提供包含資料的緩衝區。

動態緩衝區的序列化樣式使用下列常式：

-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

[**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)函式會配置編碼控制碼所需的記憶體，然後將它初始化。 應用程式可以呼叫 [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) 來重新初始化控制碼。 它會呼叫 [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) 來釋放控制碼的記憶體。 若要建立對應于動態緩衝區編碼控制碼的解碼控制碼，請使用 [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)。

 

 





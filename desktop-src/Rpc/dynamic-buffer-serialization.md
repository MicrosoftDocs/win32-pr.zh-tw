---
title: 動態緩衝區序列化
description: 使用動態緩衝區的序列化樣式時，會由存根配置封送處理緩衝區，並將資料編碼到這個緩衝區，並傳回給您。 當您進行封送時，您會提供包含資料的緩衝區。
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea47a87a9d2e566dcfb033b0c9e9403ae72081afe0a1554337dbacfef9c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021678"
---
# <a name="dynamic-buffer-serialization"></a>動態緩衝區序列化

使用動態緩衝區的序列化樣式時，會由存根配置封送處理緩衝區，並將資料編碼到這個緩衝區，並傳回給您。 當您進行封送時，您會提供包含資料的緩衝區。

動態緩衝區的序列化樣式使用下列常式：

-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

[**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)函式會配置編碼控制碼所需的記憶體，然後將它初始化。 應用程式可以呼叫 [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) 來重新初始化控制碼。 它會呼叫 [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) 來釋放控制碼的記憶體。 若要建立對應于動態緩衝區編碼控制碼的解碼控制碼，請使用 [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)。

 

 





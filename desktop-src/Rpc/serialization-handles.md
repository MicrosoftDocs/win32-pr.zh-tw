---
title: 序列化控制碼
description: 應用程式會使用由 MIDL 編譯器產生的序列化程式或序列化支援常式搭配一組程式庫函數來操作序列化控制碼。
ms.assetid: 39859846-5b94-447a-a71b-a08b8eb2c4c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12995144e44fa6b4b91f021d544b53c03d732df22d46489ccc2cefe8d34c0fa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925470"
---
# <a name="serialization-handles"></a>序列化控制碼

應用程式會使用由 MIDL 編譯器產生的序列化程式或序列化支援常式搭配一組程式庫函數來操作序列化控制碼。 這些函式一起提供一種機制，讓您自訂應用程式序列化資料的方式。

序列化作業需要序列化控制碼，而且所有序列化控制碼都必須由您明確管理。 若要這樣做，您必須先呼叫下列其中一個常式來建立有效的控制碼：

-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)

您可以呼叫 [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)來釋放控制碼。 一旦建立或重新初始化控制碼之後，它就會代表有效的序列化內容，而且可以用來編碼或解碼（視控制碼的類型而定）。

本節將說明序列化控制碼，以及如何使用它們，請前往下列主題：

-   [隱含與明確控制碼](implicit-versus-explicit-handles.md)
-   [序列化樣式](serialization-styles.md)
-   [取得編碼身分識別](obtaining-an-encoding-identity.md)

 

 





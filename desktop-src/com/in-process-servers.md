---
title: In-Process 伺服器
description: In-Process 伺服器
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccc4c65db19e4ed567a2fe6105fa4d81e9c52cc9165556d9f388d8af181eee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854528"
---
# <a name="in-process-servers"></a>In-Process 伺服器

如果您將 OLE 伺服器應用程式實作為同進程伺服器，則在容器應用程式的進程空間中執行的 DLL （而不是本機伺服器）會在其本身的進程空間中執行，因為兩者之間的通訊可能會採用一般函式呼叫的形式。 不需要遠端程序呼叫，因為這兩個應用程式會在相同的進程空間中執行。 如您所預期，管理參數封送處理的物件也是不必要的，雖然它們可能會在 DLL 內匯總，而不會干擾容器與伺服器之間的通訊。

當 OLE 伺服器應用程式實作為同進程伺服器時，不需要個別的物件處理常式，因為伺服器本身會存在於用戶端的進程空間中。 同進程伺服器和物件處理常式之間的主要差異在於，當處理常式無法時，伺服器可以管理處于執行中狀態的物件。 這項差異的其中一個結果是，伺服器必須提供使用者介面來操作執行中的物件，而處理常式則將這項需求委派給物件的伺服器。 在建立同進程伺服器的情況下，您可以在 OLE 預設處理常式上匯總，讓它在您只執行處理常式未提供或未以您所需的方式執行的服務時，處理基本的工作，例如顯示、儲存和通知。

如需詳細資訊，請參閱下列主題：

-   [優點](advantages.md)
-   [缺點](disadvantages.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[複合檔案](compound-documents.md)
</dt> </dl>

 

 





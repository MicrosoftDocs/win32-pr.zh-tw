---
description: 利用執行緒區域儲存 (TLS) ，您可以使用全域索引，為進程可以存取的每個執行緒提供唯一的資料。 一個執行緒會配置索引，其他執行緒可以使用此索引來抓取與索引相關聯的唯一資料。
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: 執行緒區域儲存區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104550768"
---
# <a name="thread-local-storage"></a>執行緒區域儲存區

一個處理序的所有執行緒都共用該處理序的虛擬位址空間。 函式的區域變數對執行函式的每個執行緒都是唯一的。 不過，靜態和全域變數會由進程中的所有線程所共用。 利用 *執行緒區域儲存* (TLS) ，您可以使用全域索引，為進程可以存取的每個執行緒提供唯一的資料。 一個執行緒會配置索引，其他執行緒可以使用此索引來抓取與索引相關聯的唯一資料。

可用的最小 TLS \_ 最小值會 \_ 定義每個進程中可用的最小 tls 索引數目。 所有系統的最小值保證至少為64。 每個進程的最大索引數目是1088。

建立執行緒時，系統會為 TLS 配置 **LPVOID** 值的陣列，這些值會初始化為 Null。 在可以使用索引之前，必須先由其中一個執行緒配置。 每個執行緒都會將 TLS 索引的資料儲存在陣列的 *tls 插槽* 中。 如果與索引相關聯的資料會符合 **LPVOID** 值，您可以將資料直接儲存在 TLS 位置中。 但是，如果您以這種方式使用大量的索引，最好是配置個別的儲存體、合併資料，並將使用中的 TLS 插槽數目降至最低。

下圖說明 TLS 的運作方式。 如需說明如何使用執行緒區域儲存區的程式碼範例，請參閱 [使用執行緒區域儲存區](using-thread-local-storage.md)。

![此圖顯示 T L S 進程的運作方式。](images/tls.png)

此處理程式有兩個執行緒，執行緒1和執行緒2。 它會配置兩個可搭配 TLS、gdwTlsIndex1 和 gdwTlsIndex2 使用的索引。 每個執行緒都會配置兩個記憶體區塊 (一個用於儲存資料的每個索引) ，然後將這些記憶體區塊的指標儲存在對應的 TLS 位置中。 為了存取與索引相關聯的資料，執行緒會從 TLS 位置抓取記憶體區塊的指標，並將其儲存在 lpvData 區域變數中。

在動態連結程式庫中使用 TLS 是很理想的 (DLL) 。 如需範例，請參閱 [使用動態連結程式庫中的執行緒區域儲存區](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[執行緒區域儲存 (Visual C++) ](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[使用執行緒區域儲存區](using-thread-local-storage.md)
</dt> <dt>

[使用動態連結程式庫中的執行緒區域儲存區](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 

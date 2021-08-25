---
title: 非同步複合檔案
description: 非同步複合檔案是系統提供的非同步儲存體執行，可讓您在一般情況下有效率地從網際網路下載複合檔案。
ms.assetid: 6cad074e-07a8-434f-a402-e29cb66a1a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15404f33041fb52f5baa5230f69434ce390b985c41374235c1f3979ef6c2f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034981"
---
# <a name="asynchronous-compound-files"></a>非同步複合檔案

非同步複合檔案是系統提供的非同步儲存體執行，可讓您在一般情況下有效率地從網際網路下載複合檔案。 非同步複合檔案的基本架構如下圖所示。

![非同步複合檔案基本架構](images/asy-stor.png)

非同步複合檔案執行可以使用新的非同步標記型別，以瞭解網際網路通訊協定，並且可以系結至 URL 所識別的物件。 這類的標記會從用戶端對 [**IMoniker：： BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage)的呼叫傳回非同步 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)或 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)指標。

一般的複合檔案會在位元組陣列物件之上執行，這是以一般位元組陣列表示物件資料的檔案抽象概念。 位元組陣列物件會透過 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) 介面公開其功能。 如果位元組陣列支援非封鎖式非同步存放裝置，它會將暫止的檔案 \_ 傳回給複合檔案的執行，然後再將錯誤傳播回呼叫端。

若要追蹤在下載期間可用的資料，支援非同步儲存的位元組陣列會在系統提供的包裝函式物件上公開 [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) 介面，這是專為此用途而設計的。 非同步標記所提供的下載程式代碼會呼叫這個介面，以非同步方式填滿位元組陣列，因為資料可供使用。 包裝函式物件也會公開 **ILockBytes** 介面，而非同步複合檔案的執行會使用此介面來讀取和寫入陣列中的資料。

非同步儲存和資料流程物件提供 [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) 介面的連接點，該介面是由非同步標記下載程式代碼所執行。 非同步複合檔案執行會呼叫 **IProgressNotify** ，以提供下載作業狀態相關資訊給下載程式。

 

 
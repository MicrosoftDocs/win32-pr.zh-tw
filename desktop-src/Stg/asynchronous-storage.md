---
title: 非同步存放裝置
description: 非同步存放裝置可增強 COM 結構化儲存規格，以支援在高延遲的低速連結網路（例如網際網路）上非同步下載儲存物件。
ms.assetid: 12b97059-2c8c-4712-8a76-03c3ce7094a0
keywords:
- 結構化儲存體 Strctd Stg.，非同步儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dd1d739223fb07c72de6c63ee173c316a132e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463484"
---
# <a name="asynchronous-storage"></a>非同步存放裝置

非同步存放裝置可增強 COM 結構化儲存規格，以支援在高延遲的低速連結網路（例如網際網路）上非同步下載儲存物件。 非同步存儲可讓使用複合檔案的新舊應用程式，在透過現有的網際網路通訊協定存取時有效地轉譯其內容。 對 World Wide Web 服務器的單一要求會觸發網頁內所包含的嵌套物件下載，而不需要個別要求每個物件。 非同步下載和存取機制可讓應用程式在收到所有資料之前，轉譯第一頁的資料。 Web 發行者可以指定頁面元素的確切順序，而不會相依于網路拓朴和伺服器可用性的隨機因素。

非同步存放裝置可與非同步名字區一起運作，以提供完整的非同步系結行為。 如需非同步名字組的詳細資訊，請參閱 Microsoft ActiveX 軟體發展工具組。 通訊協定特定的非同步標記會觸發系結作業，並設定必要的元件。 在網際網路案例中，此標記可以剖析 URL 以系結至物件或儲存體。 如果系結作業的目標是持續性物件，則呼叫 [**IMoniker：： BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) 會傳回非同步儲存物件。

> [!Note]  
> Microsoft URL 名字標記的目前版本不支援非同步存放裝置。

 

非同步標記用戶端會藉由執行系結狀態回呼物件，並向系結內容註冊來要求非同步系結。 系結狀態回呼物件會公開 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) 介面，此介面可讓用戶端指定系結喜好設定，並在系結作業過程中接收進度和全域資料可用性通知。 非同步複合檔案執行提供 [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify)的連接點，用戶端可以使用此連接點來接收個別資料流程的特定可用性通知。

 

 
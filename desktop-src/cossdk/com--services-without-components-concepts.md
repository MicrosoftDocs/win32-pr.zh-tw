---
description: COM + 1.5 引進了在沒有元件的情況下使用 COM + 服務的能力。
ms.assetid: da93d164-234a-4d1e-b82c-f3f904bb8cb6
title: 沒有元件概念的 COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d692657d33143b9437a9c8134260a8c32431cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847509"
---
# <a name="com-services-without-components-concepts"></a>沒有元件概念的 COM + 服務

COM + 1.5 引進了在沒有元件的情況下使用 COM + 服務的能力。 這可大幅降低從未使用元件的環境使用 COM + 服務時所產生的效能成本，也可以消除使用這些服務的複雜度。 從 IIS 6.0 開始，IIS 和 ASP 利用沒有元件的 COM + 服務。

COM + 服務原本是設計來搭配 COM + 元件使用。 不過，某些程式設計環境不是以元件為基礎，因此需要使用 COM + 服務的大量額外負荷。 例如，在 COM + 1.5 發行之前，IIS 必須單獨建立填充碼物件，才能在 ASP 頁面中使用 COM + 交易服務。 建立這些物件的效能成本包括將設定資料儲存在 IIS 的中繼資料和 COM + 註冊資料庫中 (RegDB) 以及 IIS 中繼資料與 COM + + RegDB 之間的額外通訊，以有效管理設定資料。

如果 IIS 需要使用第二個 COM + 服務，例如同步處理，則必須建立完全不同的填充碼物件來執行此作業。 若要同時使用 COM + 交易與同步處理，則需要第三種類型的填充碼物件。 這種方法的複雜度會隨著 O (n2) ，使新服務的執行極為困難。

由於引進的 COM + 服務沒有元件，所需的服務是透過從類別具現化的物件來設定。 [**CServiceConfig**](cserviceconfig.md)類別會執行設定不同服務所需的介面，同時提供同時支援多個服務的彈性，以及未來支援新服務的能力。

接著，您可以透過兩種不同的機制來使用設定的服務：它們可透過 [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) 函式使用，這會將服務套用至透過函式所建立之活動提交的所有工作，而且也可以藉由在 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) 和 [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) 函數的呼叫之間內嵌使用服務的工作來使用。 這些函式都不需要建立任何新元件，就能使用 COM + 服務;只需要 [**CServiceConfig**](cserviceconfig.md) 物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[沒有元件工作的 COM + 服務](com--services-without-components-tasks.md)
</dt> </dl>

 

 




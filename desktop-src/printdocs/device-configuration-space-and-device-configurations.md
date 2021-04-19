---
title: 裝置設定空間
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120e12b6480675dba6e735390f4820a8782edc5c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "107000349"
---
# <a name="device-configuration-space-and-device-configurations"></a>裝置設定空間和裝置設定

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

裝置的設定 *空間* 是所有可能值的集合，可指派給裝置的所有屬性。 在 PrintCapabilities 中描述裝置設定空間的兩個最重要的原因如下所示。

1.  這項資訊可大幅提升對裝置功能的瞭解。 這項資訊可讓 PrintCapabilities 的用戶端輕鬆地產生使用者介面 (UI) 元素，讓使用者更容易選取特定的設定來處理作業。 藉由提供應用程式的更多詳細資料，以及最終使用者的功能，使用者的列印意圖可以更有效率地完成。

2.  PrintCapabilities 中顯示的某些裝置屬性可能會取決於用戶端選取的特定設定。

部分資訊不應併入 PrintCapabilities 中。 這包含的資訊不會影響作業的建立方式、不會限制建立作業的方式，也不會影響裝置屬性。 例如，裝置可能會報告狀態資訊，例如等待處理的作業集合。 這項資訊不會影響格式化作業所需的資訊，也不會提供裝置中可用功能的任何指示。 基於這個理由，PrintCapabilities 中不需要有這種類型的資訊。

## <a name="device-constraints"></a>裝置條件約束

由於裝置上的條件約束，許多裝置不支援設定空間中的所有可能設定。 例如，裝置可能會受到限制，無法在透明媒體上執行雙工列印。 條件約束可代表實體限制：某些媒體類型的內容太過嚴格，無法流經裝置中的特定紙張路徑，因此不能放在某些輸入位置或路由傳送至某些輸出的位置。目前，PrintCapabilities 或 PrintTicket 提供者必須負責驗證輸入 PrintTicket 所代表的設定，以確認它不代表不正確設定。 如果設定無效，PrintCapabilities 或 PrintTicket 提供者應該以使設定變成有效的方式修改設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




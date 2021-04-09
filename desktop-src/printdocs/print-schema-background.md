---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: 列印架構背景
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93280b6c8de62c76acdd59e2e596a0f600702451
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103696326"
---
# <a name="print-schema-background"></a>列印架構背景

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

列印架構的目的是要解決與列印子系統元件之間的內部通訊相關的 opaqueness 和不明確的問題，以及列印子系統和應用程式之間的外部通訊。

目前的列印子系統與應用程式和硬體廠商的外掛程式互動會使用二進位、以索引為基礎的 DEVMODE 結構和二進位 DevCaps。 每個元件所做的設定，對其他元件來說大多是不透明的，防止裝置之間的設定可攜性，甚至在相同裝置上的不同驅動程式版本之間可移植。 此外，用戶端應用程式不需要對裝置有專屬的知識，或使用驅動程式使用者介面 (UI) ，就不容易利用 PrintCapabilities。 除了這些限制之外，沒有定義完善的語言來描述一般裝置屬性、PrintCapabilities、裝置設定或作業格式。 列印架構及其相關技術的設計目的是要解決這些限制，並以合併和邏輯的方式，提供一致、明確且可擴充的設定與功能通訊方法。

Print Schema 關鍵字和 Print Schema Framework 的概念基礎是一致的，缺乏不明確的擴充性。 一致性是透過使用 Print Schema 關鍵字和 Print Schema Framework 來達成，以作為下一代列印元件之間的通訊基礎結構。 應用程式、Microsoft Windows 列印子系統以及 IHV 外掛程式和驅動程式都會使用此常見機制進行互動。 這些關鍵字、其結構和其意義將由公用架構妥善定義。 這可防止特定關鍵字的意義不明確，並可避免重複或重複的關鍵字。 所有元件都可以依賴使用特定關鍵字來傳達特定意圖，並讓收件者充分瞭解該意圖。 擴充性的關鍵是列印架構關鍵字的壽命，以確保公用架構為動態實體。 此結構也允許私用延伸模組，可授與 Ihv 可依需求創新的彈性，並記得未來將私用關鍵字納入公用架構中，是保留一致性和避免混淆的必要。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




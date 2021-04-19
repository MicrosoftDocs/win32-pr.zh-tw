---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: 列印架構公用關鍵字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3e8fb9a46bbed2b135f4e81456dd65e79be830
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986684"
---
# <a name="print-schema-public-keywords"></a>列印架構公用關鍵字

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

下一節指定針對列印架構定義的公用關鍵字。

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a>列印功能的列印架構公用關鍵字用法

在 PrintCapabilities Public 關鍵字下指定的關鍵字可能會顯示在列印功能檔中。 如需這些關鍵字如何與 PrintCapabilities 技術互動的詳細資訊，請參閱 [PrintCapabilities](overview-of-the-printcapabilities.md) 一節的總覽。

PrintTicket 專屬的公用關鍵字不應該出現在 PrintCapabilities 檔中。

## <a name="print-schema-public-keywords-usage-for-printticket"></a>列印 PrintTicket 的架構公用關鍵字用法

在 PrintTicket Public 關鍵字下指定的關鍵字可能會出現在 PrintTicket 中。 PrintTicket 關鍵字會實作為屬性元素類型。 如需這些關鍵字如何與 PrintTicket 技術互動的詳細資訊，請參閱與 PrintCapabilities 無關的設定 [資訊](configuration-information-not-related-to-printcapabilities.md) 一節。

在 PrintCapabilities Public 關鍵字下指定的關鍵字，可能會根據應用程式和（或）驅動程式中的 PrintTicket 執行而出現在 PrintTicket 中。 這會針對 PrintCapabilities 檔中定義的裝置屬性提供選取專案。 如需 PrintCapabilities 關鍵字與 PrintTicket 之間互動的詳細資訊，請參閱 PrintTicket 區段的 [用途](purpose-of-the-printticket.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




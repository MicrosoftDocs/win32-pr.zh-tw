---
description: 瞭解如何加入屬性實例。 列印架構可讓屬性實例存在於選項實例中。
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: 加入屬性實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8085fa10f824f32dc76aef0f1e5f78ca05b22b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409691"
---
# <a name="adding-property-instances"></a>加入屬性實例

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

列印架構可讓屬性實例存在於選項實例中。 PrintCapabilities 檔中定義的屬性實例不會傳播至儲存在 PrintTicket 中的選項實例。 比較兩個選項實例時，屬性專案不會影響評分進程的結果，但 ScoredProperty 實例會影響此程式。 所有執行評分演算法的設備磁碟機都應該遵守此慣例。 如果這些實例是特定選項以外的特定選項，或如果提供者打算針對功能中的每個選項顯示這個屬性的值，則 PrintCapabilities 提供者可以將屬性實例加入至選項。 例如，假設 PrintRate 屬性相依于針對 PageResolution 功能選取的選項。 如果 PrintRate 屬性是放在 PrintCapabilities 檔的根層級，它會是單一值，而且只會反映目前所選解析度的列印速率。 但是，如果 PrintRate 屬性是放置在每個 PageResolution 選項內，則 PrintRate 屬性的每個實例都可以反映包含它之 PageResolution 選項的列印速率。 PrintCapabilities 檔會包含 PrintRate 的多個定義，一個對應至每個 PageResolution 選項。 使用速記標記法時，PrintCapabilities 會包含：

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

在某些情況下，在每個解析度選項中放置列印速率屬性，對於用戶端來說更方便，因為用戶端可以判斷每個解析度選項對列印速率的影響，而不需要為每個解析度設定取得新的 PrintCapabilities 檔。

另外也請注意，屬性實例也可以新增為功能專案的子項目。 如果每個功能都有特定屬性實例或屬性實例的值，這就很有用。 例如，可能會有一個屬性，指定某項功能一次只允許選取一個選項，還是可以選取多個選項。 這是挑選 \_ 一個，挑選 \_ 許多用於 PPD 和 GPD 檔案的屬性。 因為某些功能實例可能會被識別為挑選 \_ 一個，而有些則可能被視為挑選 \_ 許多，所以必須為每項功能定義這個屬性。 將屬性尋找為功能的子專案，會產生屬性和功能之間的關聯。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




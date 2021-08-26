---
description: 瞭解如何參考參數和 ParameterDef 元素。 包含 ParameterRef 元素的選項範例是自訂媒體大小選項。
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: 參考參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def14223c2d1a4471582e28881a3784eb86239e8daec0e9ec63bff8bc8b7838a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112138"
---
# <a name="referencing-parameters"></a>參考參數

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

包含 ParameterRef 元素之選項的具體範例是自訂媒體大小選項。 請注意，它會參考兩個參數： PageMediaSizeMediaSizeWidth 和 PageMediaSizeMediaSizeHeight。 每個 ParameterRef 實例都會參考 PrintCapabilities 檔中其他位置所定義的 ParameterDef 實例。 如需 ParameterDef 元素的詳細資訊，請參閱 [ParameterDef](parameterdef.md)。 如需有關定義參數的概念資訊，請參閱 [ParameterDef 和 ParameterInit 元素](parameterdef-and-parameterinit-elements.md)。

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

只是要建立參數化選項，以確保會正確處理和處理選項。 PrintCapabilities/PrintTicket 提供者和用戶端必須提供其他支援，才能正確地執行參數化選項實例。 下列各節將說明所需的行為。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




---
description: 阿拉伯文和許多其他語言都具有傳統的數位圖形，與最常用於電腦的傳統西方數位不同。
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: 數位形狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980002"
---
# <a name="digit-shapes"></a>數位形狀

阿拉伯文和許多其他語言都具有傳統的數位圖形，與最常用於電腦的傳統西方數位不同。 為了避免對這些圖形命名有不明確的情況，本檔會使用 Unicode 標準的下列名稱。



| 數位的 Unicode 名稱                                     | 使用的國家/地區                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| 歐洲數位                                                | 歐洲、美洲及許多其他國家/地區       |
| Arabic-Indic 數位                                            | 阿拉伯文國家/地區 (雖然有許多使用歐洲位數)  |
| 其他國家/地區數位：印度文數位、泰文數位和 like | 不同國家/地區                                    |



 

Unicode 為每個數位圖形提供個別的程式碼點。 因此，若要存取特殊語言數位圖形，您的應用程式可以針對上述數位使用相關的 Unicode 字元碼，U + 0030 到 U + 0039。 這些代碼一律會以適當的圖形顯示，且受限於字型的可用性。

Unicode 字元碼 U + 0030 到 U + 0039 名義上表示歐洲數位0到9，但可以改變其數位圖形。 GDI 和 DirectWrite 文字 Api 提供應用程式控制此行為的機制。  (請參閱，例如 [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) 或 [**IDWriteTextAnalysisSink：： SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution)。 ) 某些 shell 控制項和使用者介面架構中的行為，可能會回應使用者地區設定的數位替代; [地區設定 \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE 可以用來取得不同地區設定的預設數位替代設定，或用於數位替換的目前使用者桌面設定。

## <a name="native-digits"></a>原生位數

原生位數是使用者在主控台的 [地區及語言選項] 部分的 [ **數位** ] 屬性工作表中選擇的數位形狀。 若要尋找使用者慣用的數位標記法，您的應用程式會使用 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 函式搭配 [地區設定 \_ SNATIVEDIGITS](locale-snative-constants.md) 常數來表示地區設定資訊。

> [!Note]  
> 通常，Unicode 數位代碼會在執行時間作業系統常式中產生。 因此，必須升級一般執行時間作業系統，應用程式才能適當地檢查 [地區設定 \_ SNATIVEDIGITS](locale-snative-constants.md) 。

 

## <a name="digit-substitution"></a>數位替換

應用程式可以使用數位替代來告訴作業系統如何透過 U + 0039 列印數位 U + 0030。 [地區設定 \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md)常數控制這種作業。

## <a name="digit-shaping-for-a-single-function"></a>單一函式的數位成形

[ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta)、 [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)和[GCP \_ 結果](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa)函式具有旗標，可在函式呼叫期間管理 Unicode 程式碼 U + 0030 至 u + 0039 的替代。 這些旗標會覆寫主控台中的地區設定，但不會重設設定。 此外，它們不會覆寫 Unicode 代碼 NADS 和節點。 以下是可用的旗標。



| Flags                 | 使用的數位                      | 使用於                   |
|-----------------------|----------------------------------|---------------------------|
| ETO \_ NUMERICSLATIN    | 歐洲數位                  | **ExtTextOut**            |
| ETO \_ NUMERICSLOCAL    | 適用于地區設定的數位 | **ExtTextOut**            |
| GCP \_ NUMERICSLATIN    | 歐洲數位                  | **GetCharacterPlacement** |
| GCP \_ NUMERICSLOCAL    | 適用于地區設定的數位 | **GetCharacterPlacement** |
| GCPCLASS \_ LATINNUMBER | 歐洲數位                  | **GCP \_ 結果**          |
| GCPCLASS \_ LOCALNUMBER | 適用于地區設定的數位 | **GCP \_ 結果**          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於國家語言支援](about-national-language-support.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 

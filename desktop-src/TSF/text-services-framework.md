---
title: '文字服務架構 (文字服務架構) '
description: Microsoft Windows 文字服務架構 (TSF) 是一種系統服務，可作為 Windows 2000 的可轉散發套件。
ms.assetid: ecc34b2e-89e8-48a8-8a8e-442d2145fe24
ms.topic: article
ms.date: 01/14/2020
ms.openlocfilehash: 9c21cae442b5fbed62c00010a17849d1d5f27b49
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685380"
---
# <a name="text-services-framework-text-services-framework"></a>文字服務架構 (文字服務架構) 

## <a name="purpose"></a>目的

Microsoft Windows 文字服務架構 (TSF) 是一種系統服務，可作為 Windows 的可轉散發套件。 TSF 提供簡單且可擴充的架構，可提供先進的文字輸入和自然語言技術。 TSF 可在應用程式中啟用，也可以在 TSF 文字服務中啟用。 TSF 文字服務可提供多語系支援並傳遞文字服務，例如鍵盤處理器、手寫辨識和語音辨識。

## <a name="where-applicable"></a>適用時

文字服務架構適用于使用文字服務和 Windows XP 或更新版本作業系統的 Windows 電腦。

## <a name="developer-audience"></a>開發人員對象

文字服務架構的設計目的是要讓元件物件模型使用 C/c + + 程式設計語言 (COM) 程式設計人員使用。 程式設計人員應該熟悉 Windows 電腦的文字服務。 建議您瞭解手寫辨識、語音辨識，以及多語系支援的程式設計。

## <a name="run-time-requirements"></a>執行階段需求求

如需最新的可轉散發套件，請下載 [Windows 10 PLATFORM SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)。

如需特定 API 元素需求的詳細資訊，請參閱 < (/windows/win32/tsf/text-services-framework-reference) [TFS 參考檔] 中的需求一節。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                 | 描述                                                                                                      |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [關於文字服務架構](about-text-services-framework.md)<br/>         | 文字服務架構的一般資訊。<br/>                                                    |
| [使用文字服務架構](using-text-services-framework.md)<br/>         | 使用文字服務架構的相關資訊。<br/>                                                      |
| [文字服務架構參考](text-services-framework-reference.md)<br/> | 文字服務架構介面、方法、結構和其他程式碼元素的相關檔。<br/> |
| [詞彙](glossary.md)<br/>                                                   | 本檔中所使用的技術詞彙清單（依字母順序排列）。<br/>                                   |



 

## <a name="additional-resources"></a>其他資源

閱讀本指南之前，您應該知道的事項

基於文字服務架構說明的目的，「應用程式」一詞是指已啟用 TSF 的應用程式，「文字服務」一詞指的是 TSF 文字服務，「經理」一詞指的是 TSF 管理員。 除非另有指定，否則每個詞彙都適用于此處所述。 文字服務提供者應該提供數位簽章給其二進位可執行檔。

 

 






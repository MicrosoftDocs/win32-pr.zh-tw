---
description: 使用字型回復
ms.assetid: 952f33b6-ca52-40a2-b914-52c1c62ae0e0
title: 使用字型回復
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9a4e9b329e2c3257ae9fad02f1fb4774a63dc1d4b4e804c0dca8e690cbf4d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787868"
---
# <a name="using-font-fallback"></a>使用字型回復

> [!Note]  
> 在本主題中，所有關于 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 的備註都同樣適用于 [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)。

 

如果字型中不支援字串中的某些字元，或如果應用程式使用字型不支援的 [複雜字集](uniscribe-glossary.md) ，則您的應用程式必須在文字顯示期間使用字型回復。 當應用程式呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 函式時，會在文字的版面配置程式期間偵測到字型回復的需求。 如需文字顯示的詳細資訊，請參閱 [使用 Uniscribe 來顯示文字](displaying-text-with-uniscribe.md)。

## <a name="determine-the-need-for-font-fallback-for-unsupported-characters"></a>判斷支援的字元是否需要字型回復

如果要求的字型不支援字串中的某些字元，則 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 的應用程式呼叫會成功。 不過，應用程式必須掃描圖像輸出緩衝區是否有遺漏的圖像。 您可以藉由呼叫 [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)，判斷特定字型的圖像索引。 如果無法使用特定的圖像，應用程式必須切換回圖像的不同字型，或轉譯表示沒有可用字元的圖形符號。

## <a name="determine-the-need-for-font-fallback-for-unsupported-complex-scripts"></a>針對不支援的複雜字集，判斷字型回復的需求

應用程式慣用的顯示字型可能不支援文字所需的複雜字集。 在此情況下，對 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 的應用程式呼叫會失敗，並出現錯誤碼 E \_ 腳本的 \_ 非 \_ \_ 字型。

## <a name="assign-a-fallback-font"></a>指派回復字型

一旦判斷出需要字型回復之後，應用程式就必須指派回復字型。 應用程式可以嘗試下列技術：

-   針對字型清單中的每個字型呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ，直到一個呼叫具有可接受的傳回。
-   使用清單中的每個字型來呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ，直到判斷任何字型都不會成功為止。 如果錯誤碼一律為 E \_ SCRIPT \_ not \_ \_ 字型，字型就不支援複雜的腳本。 轉譯圖形符號，指出沒有任何可用的圖像，或將腳本重新指定為未定義 (沒有腳本處理) ，然後重新開機。 若要將腳本設定為未定義，請將 [**腳本 \_ 分析**](/windows/win32/api/usp10/ns-usp10-script_analysis)結構的 **eScript** 成員設定為 \_ 未定義腳本。
-   使用清單中的每個字型來呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ，直到判斷任何字型都不會成功為止。 如果錯誤碼指出某些字元是對應至遺失的字元，請將字串分解為較小的範圍。 您可以將不同的字型指派給子範圍，讓更多的字元可以呈現。

## <a name="generate-glyph-information"></a>產生符號資訊

一旦應用程式指派了成功呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)的字型之後，就可以呼叫 [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) ，從 **ScriptShape** 的輸出產生圖像前進寬度和二維位移資訊。 在這些呼叫中，字型應該會成功。 在 **ScriptShape** 呼叫成功後呼叫 **ScriptPlace** 的字型失敗，表示有不正確字型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




---
title: HLSL 的參考
description: HLSL 參考檔會指定語言特性。 它分成數個部分。
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021835"
---
# <a name="reference-for-hlsl"></a>HLSL 的參考

HLSL 參考檔會指定語言特性。 它分成數個部分。

-   [語言語法 (DIRECTX HLSL) ](dx-graphics-hlsl-language-syntax.md) -HLSL 中的程式設計著色器需要您瞭解語言語法，也就是撰寫 HLSL 程式碼的方式。 這包括用來宣告和初始化變數、撰寫使用者定義著色器函式的程式碼，以及新增流程式控制制語句，讓您的函式更具強大功能。
-   [著色器模型與著色器設定檔](dx-graphics-hlsl-models.md) -HLSL 編譯器會根據著色器模型來實行規則和限制。 每個頂點著色器中的程式碼、幾何著色器 (如果您使用 Direct3D 10) 和圖元著色器是針對您在編譯時期提供的著色器模型進行驗證。
-   [**內建函式 (DIRECTX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) -HLSL 有許多內建函式。 這些會經過執行和測試，讓您可以使用它們來瞭解它們已經過調試，而且表現正常。 如果您選擇撰寫自己的函式，請參閱撰寫使用者定義函數的語言語法一節。
-   [Asm 著色器參考](dx9-graphics-reference-asm.md) -您可以用來程式設計和調試著色器的元件指令。
-   [D3DCompiler 參考](dx-graphics-d3dcompiler-reference.md) -編譯原始 HLSL 來源。
-   [內嵌格式轉換參考](inline-format-conversion-reference.md) -D3DX \_ DXGIFormatConvert. .inl 檔案包含內嵌格式轉換函式，您可以在 Direct3D 11 硬體上的計算著色器或圖元著色器中使用這些函數。 您可以在應用程式中使用這些函式，同時讀取和寫入材質。 也就是說，您可以執行就地影像編輯。 若要使用這些內嵌格式轉換函式，請將 D3DX \_ DXGIFormatConvert. .inl 檔案包含在您的應用程式中。
-   [附錄 (DIRECTX HLSL) ](dx-graphics-hlsl-appendix.md) -已包含附錄以提供完整性。 其中包含關鍵字和保留字的清單;這些字組無法當做程式中的識別碼使用。 它也包含用於參考的語言文法清單。
-   [**HLSL 錯誤和警告**](hlsl-errors-and-warnings.md) -提供著色器可傳回的錯誤和警告碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL](dx-graphics-hlsl.md)
</dt> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 





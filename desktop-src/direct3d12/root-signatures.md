---
title: 根簽章
description: 根簽章會定義要系結至圖形管線的資源類型。
ms.assetid: ee32a222-8469-4af5-b688-afa70cf77c6a
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4c034e208dd841545777cc92878e7020b9b4a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548413"
---
# <a name="root-signatures"></a>根簽章

根簽章會定義要系結至圖形管線的資源類型。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                               | 描述                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [根簽章總覽](root-signatures-overview.md)<br/>                                                 | 根簽章是由應用程式設定，並將命令清單連結至著色器所需的資源。 圖形命令清單同時具有圖形和計算根簽章。 計算命令清單只會有一個計算根簽章。 這些根簽章彼此獨立。<br/>                                                                                             |
| [使用根簽章](using-a-root-signature.md)<br/>                                                     | 根簽章是描述項資料表的任意排列集合的定義， (包括其配置) 、根常數和根描述項。 每個專案都有最大限制的成本，因此應用程式可以在根簽章將包含的每個專案類型的數目之間，權衡平衡。<br/>                                                                     |
| [建立根簽章](creating-a-root-signature.md)<br/>                                               | 根簽章是包含嵌套結構的複雜資料結構。 您可以使用下列資料結構定義，以程式設計的方式定義這些方法 (其中包含有助於初始化成員) 的方法。 或者，您也可以使用高階的陰影語言來撰寫 (HLSL) 提供的優點是編譯器會及早驗證配置與著色器的相容性。 <br/> |
| [根簽章限制](root-signature-limits.md)<br/>                                                       | 根簽章是主要房地產，而且需要考慮嚴格的限制和成本。<br/>                                                                                                                                                                                                                                                                                                            |
| [直接在根簽章中使用常數](using-constants-directly-in-the-root-signature.md)<br/>     | 應用程式可以在根簽章中定義根常數，每個常數都是一組32位值。 它們會以高階的陰影語言顯示 (HLSL) 作為常數緩衝區。 請注意，記錄原因的常數緩衝區會視為4x32 位值的集合。 <br/>                                                                                                                                        |
| [直接在根簽章中使用描述項](using-descriptors-directly-in-the-root-signature.md)<br/> | 應用程式可以直接將描述項放在根簽章中，以避免需要經過描述元堆積。 這些描述項會在根簽章中佔用大量空間 (請參閱) 的根簽章限制一節，讓應用程式必須謹慎使用它們。 <br/>                                                                                                                                     |
| [範例根簽章](example-root-signatures.md)<br/>                                                   | 下一節顯示從空白到完全完整的根目錄簽章變化。<br/>                                                                                                                                                                                                                                                                                                       |
| [在 HLSL 中指定根簽章](specifying-root-signatures-in-hlsl.md)<br/>                             | 在 HLSL 著色器模型5.1 中指定根簽章是在 c + + 程式碼中指定它們的替代方法。<br/>                                                                                                                                                                                                                                                                                                  |
| [根簽章版本1。1](root-signature-version-1-1.md)<br/>                                             | 「根簽章版本1.1」的目的是要讓應用程式在描述項的描述項堆積中的描述項變更時，向驅動程式指出，或將資料描述點變更為「獲勝」。 如此一來，驅動程式的選項就能進行優化，以瞭解描述項或所指向的記憶體在一段時間內是靜態的。 <br/>                                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> <dt>

[**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer)
</dt> <dt>

[資源系結](resource-binding.md)
</dt> </dl>

 


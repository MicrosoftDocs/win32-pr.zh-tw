---
description: 閱讀 PrintCapabilities 檔中有關參數定義的資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: 參數定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc8ad2bed3a972202bc0a5bb07cbdd4ef9d8f44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396573"
---
# <a name="parameter-definitions"></a>參數定義

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

本節將概述可能出現在 PrintCapabilities 檔中的公用參數定義。

參數是用來描述可接受的值範圍，而不是值的離散列舉。

## <a name="parameterdef"></a>ParameterDef

如需 ParameterDef 元素類型的摘要，請參閱 [ParameterDef](parameterdef.md) 一節。

如需 ParameterDef 元素與 ParameterInit 專案之間互動的詳細資訊，請參閱 [ParameterDef 和 ParameterInit 元素](./parameterdef-and-parameterinit-elements.md) 一節。

ParameterDef 在列印架構關鍵字中定義的元素必須在 PrintCapabilities 檔中完整定義。

## <a name="parameterref"></a>ParameterRef

如需 ParameterRef 元素類型的摘要，請參閱 [ParameterRef](parameterref.md) 一節。

使用者可設定的元素關鍵字可以包含參數的參考。 ParameterRef 元素會指定為 ScoredProperty 專案的子系。如需詳細資訊，請參閱 [參數參考元素](parameter-reference-elements.md) 一節。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 

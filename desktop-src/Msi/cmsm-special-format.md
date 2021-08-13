---
description: 搭配可設定合併模組使用的某些值需要特殊的文字處理。
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: CMSM 特殊格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8521c422d62980da0d222f8a8fc8395afa40b68bfd65c5600298372b1035f97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252138"
---
# <a name="cmsm-special-format"></a>CMSM 特殊格式

搭配可設定合併模組使用的某些值需要特殊的文字處理。 描述為「CMSM 特殊格式」的文字字串會將分號 (; ) 和 equals (=) 字元作為用戶端合併工具或 Mergemod.dll 所使用的保留字元。

下列位置目前使用 CMSM 的特殊格式：

-   [ModuleSubstitution 資料表](modulesubstitution-table.md)的資料列資料行。
-   [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行。
-   當位在 Format 資料行中的值時， [ModuleConfiguration 資料表](moduleconfiguration-table.md) 的 CoNtextData 資料行。
-   當 Text 是 Format 資料行中的值，而 Enum 是 Type 資料行中的值時， [ModuleConfiguration 資料表](moduleconfiguration-table.md) 的 CoNtextData 資料行。
-   當索引鍵是 Format 資料行中的值時， [ModuleConfiguration 資料表](moduleconfiguration-table.md) 的 DefaultValue 資料行。
-   [**ProvideTextData 方法**](configuremodule-providetextdata.md)所使用之金鑰格式的可設定專案。

若要以 CMSM 特殊格式輸入常值分號或等號字元，請在字元前面加上反斜線字元 ( ' \\ ' ) 。 常值反斜線可以用兩個反斜線表示。 前置詞為單一反斜線的單一字元會轉譯成單一字元，即使不需要將字元轉義也是一樣。

如果分號或等於字元沒有前置詞，但在值的內容中沒有定義的行為，則產生的字串會是未定義的。 例如，ModuleConfiguration 資料表的 DefaultValue 資料行是所有索引鍵專案的 CMSM 特殊格式，因為分號字元是資料行分隔符號。 雖然在此字串中，等號字元沒有特殊意義，但常值相等的字元仍然必須在此字串中進行轉義。

 

 




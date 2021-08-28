---
title: 音訊壓縮管理員函式和結構
description: 音訊壓縮管理員函式和結構
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- 多媒體音訊、正常運作
- 音訊、等式函數
- 音訊壓縮管理員 (的功能) 、函式
- " (音訊壓縮管理員) 、函式、功能"
- 多媒體音訊、進行中的結構
- 音訊、進行中的結構
- 音訊壓縮管理員 (的) 、結構
- " (音效壓縮管理員) 、結構"
- 進行中結構
- 進行的函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabd9a66bee13c02c87df95565744eb973283baedb7e955449feb2ddad3005a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808378"
---
# <a name="audio-compression-manager-functions-and-structures"></a>音訊壓縮管理員函式和結構

執行的函式分成數個類別。 函數的命名慣例可讓您輕鬆地識別這些類別。 函式名稱 (有兩個例外狀況) 的形式為 *acmGroupFunction*，其中 *Group* 會指定 ([FormatTag]、[格式]、[]、[篩選]、[FilterTag] 或 [資料流程] ) *，且函* 式會描述函式所執行的動作。

篩選和格式群組中的函數非常類似。 幾乎每個在篩選上作用的函式都有平行函式，可針對格式進行作用。

在 format 群組中，某些函式會使用波形-音訊格式標記 ([**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)) 結構的 **wFormatTag** 成員，而其他函式則需要完整的波形音訊格式 (完整的 **WAVEFORMATEX** 結構) 。  (如需 **WAVEFORMATEX** 結構的參考資訊，請參閱 [錯誤](error.md)。 ) 

在篩選群組中，某些函式會使用波形-音訊篩選標記 ([**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter)) 結構的 **dwFilterTag** 成員，而其他函式則需要完整的波形音訊篩選 (完整的 **WAVEFILTER** 結構) 。

資料流程群組中的函式代表與轉換有關的許多步驟：開啟轉換實例、準備轉換、執行轉換、在轉換完成之後清除，以及關閉轉換實例。

 

 
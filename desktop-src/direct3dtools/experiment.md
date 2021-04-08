---
description: 表示實驗 (capture) 的相關資訊。
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 實驗結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687899"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span id="vspixengine.experiment"></span>實驗結構

表示實驗 (capture) 的相關資訊。

## <a name="syntax"></a>語法


```C++
} Experiment;
```

## <a name="members"></a>成員

**進程**  
相關聯的處理序識別碼。

**applicationName**  
COM 字串，其中包含要執行實驗的應用程式名稱。

**commandLineArguments**  
包含命令列引數的 COM 字串。

**workingDirectory**  
包含工作目錄路徑的 COM 字串。

**tempPixRunFile**  
COM 字串，其中包含用來執行實驗之暫存檔案的 filepath。

**startOption**  
與實驗相關聯的啟動選項。

**experimentType**  
 (capture) 的實驗類型。

**uiLocale**  
Experiement (capture) 期間，用於 UI 重迭元素的地區設定識別碼。 這會從主機 (（例如 Visual Studio 圖形診斷) 傳遞至 capture 引擎）。

**registryRoot**  
包含登錄根目錄的 COM 字串。 這會從主機 (（例如 Visual Studio 圖形診斷) 傳遞至 capture 引擎）。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 




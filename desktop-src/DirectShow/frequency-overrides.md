---
description: 頻率覆寫
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: 頻率覆寫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a2c7663e70aa0e975cee52dc630453bea1ad4121a8c91d03564fe7d7a2cb4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997837"
---
# <a name="frequency-overrides"></a>頻率覆寫

花費大量的精力來確保每個國家/地區的廣播頻率和色彩標準指派都是正確的。 儘管如此，在某些情況下，頻率資料表還不夠、包含錯誤或淘汰。 若要解決這個問題，可以使用下列登錄機碼，選擇性地覆寫 TV 調諧器篩選準則的頻率資料表中所列的頻率：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **電視 System Services** \\ **TVAutoTune** \\ **TS0-1**

> [!Note]  
> 從 Windows 7 開始，下列重新導向的登錄機碼會用於在 x64 版本的 Windows 上執行的 x86 應用程式：

 

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Wow6432Node** \\ **Microsoft** \\ **電視 System Services** \\ **TVAutoTune** \\ **TS0-1**

頻率覆寫會分組為應用程式定義的「微調空間」，並以數位來識別。 下列範例顯示範例覆寫：

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

在此情況下，「TS0-1」表示微調空間的空間為0。 第一個數位會識別微調空間。 第二個數字是針對廣播頻率為0，而針對纜線頻率為1。

名為 "12" 的子機碼會覆寫目前頻率資料表中索引12的頻率值。 子機碼的值是一個 **DWORD** ，可指定以赫茲 (Hz) 的頻率。 在此範例中，頻率設為 67.25 MHz。 您可以針對範圍介於1到999（含）的任何通道編號定義覆寫。 如果微調硬體不支援指定的頻率，微調要求將會失敗。

這項機制也可以用來在 frequency 資料表中的現有範圍之外建立新的通道號碼。 [**IAMTuner：： ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax)方法會傳回擴充的通道範圍。 例如，如果原始通道範圍是1到158，而將 "200" 的通道覆寫新增至登錄，則 **ChannelMinMax** 方法會傳回200作為最大通道。 在此情況下，159到199範圍中的通道編號不會指派任何頻率，因此該範圍內的任何微調要求都會自動失敗。

[**IAMTuner：:p \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace)方法可讓應用程式選擇要使用的一組覆寫和微調資訊。 微調空間數目是任意的。 應用程式必須負責維護微調空間與頻率資料表之間的關聯性。 最直接的方法是使用國家/地區碼作為微調空間號碼。 然後，每次應用程式切換至新的國家/地區代碼時，也會切換至相同的微調空間 (順序) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[國際類比電視微調](international-analog-tv-tuning.md)
</dt> </dl>

 

 




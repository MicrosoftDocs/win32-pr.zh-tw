---
title: Echo 範例如何保存資料
description: Echo 範例如何保存資料
ms.assetid: be75760f-c378-45d1-99de-43ef0ec4b8f0
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df781754fd52639272850158187cb1258c081583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673907"
---
# <a name="how-the-echo-sample-persists-data"></a>Echo 範例如何保存資料

當 Windows Media Player 啟用 DSP 外掛程式時，它可能會在會話過程中建立和終結外掛程式物件的許多實例。 外掛程式需要一種方式來保存實例之間的屬性值。 Windows Media Player 外掛程式 Wizard 產生的範例程式碼會將這些值儲存在登錄中，並在叫用屬性頁或建立外掛程式的新實例時，抓取這些值。

Echo 中的預設範例程式碼包含兩個常數，可儲存預設登錄路徑和擴展因數名稱字串。 您應該保留指定路徑的變數，但刪除指定小數位數登錄名稱的程式程式碼。 然後，新增下列程式碼來定義延遲時間的常數，並在登錄中將屬性名稱加上濕。 完成的區段應該會顯示如下：


```C++
// registry location for preferences
const TCHAR kszPrefsRegKey[] = _T("Software\\Echo\\DSP Plugin");
const TCHAR kszPrefsDelayTime[] = _T("DelayTime");
const TCHAR kszPrefsWetmix[] = _T("Wetmix");

```



當您修改屬性頁方法時，將會使用這些常數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**修改 Echo 範例屬性頁**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





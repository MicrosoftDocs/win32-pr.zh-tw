---
description: ELS 腳本偵測服務稱為 Microsoft 腳本偵測。
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Microsoft 腳本偵測
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114196"
---
# <a name="microsoft-script-detection"></a>Microsoft 腳本偵測

ELS 腳本偵測服務稱為 Microsoft 腳本偵測。 這項服務可讓應用程式偵測寫入文字的腳本。  (NLS) 對應的「腳本偵測」服務的國家語言支援是 [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) 函數。 不過，ELS 服務會另外抓取屬於每個書寫系統的文字範圍。

## <a name="input-to-microsoft-script-detection"></a>輸入至 Microsoft 腳本偵測

Microsoft 腳本偵測服務的輸入是由服務決定腳本範圍的 UTF-16 文字。

## <a name="output-of-microsoft-script-detection"></a>Microsoft 腳本偵測的輸出

Microsoft 腳本偵測服務的輸出是範圍的陣列，每個都包含以 null 終止的 UTF-16 字串，且具有相關聯書寫系統的 Unicode 指定名稱。 這項服務會報告一般常見的 (Zyyy) ，並將 () 字元繼承為屬於先前的腳本範圍。 開始通用和繼承的字元會回報為屬於下一個腳本範圍。 如果輸入文字中的所有字元都是通用或繼承的，則服務的輸出會是具有空字串作為其資料的單一範圍。

## <a name="microsoft-script-detection-operation"></a>Microsoft 腳本偵測操作

Microsoft 腳本偵測服務會將屬於通用範圍的程式碼點對應到上述的寫入系統。 或者，如果程式碼點位於輸入字串的開頭，則服務可以將程式碼點對應到下一個寫入系統。 應用程式完全不需要處理通用範圍。

## <a name="microsoft-script-detection-guid"></a>Microsoft 腳本偵測 GUID

Microsoft 語言偵測服務的 GUID 是在 Elssrvc 中宣告，如下列程式碼所示。


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於擴充的語言服務](about-extended-linguistic-services.md)
</dt> </dl>

 

 




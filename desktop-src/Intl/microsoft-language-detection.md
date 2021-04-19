---
description: ELS 語言偵測服務稱為 Microsoft 語言偵測。 這項服務會使用 Microsoft 專利技術，讓應用程式能夠偵測撰寫特定文字的語言。
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Microsoft 語言偵測
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974339"
---
# <a name="microsoft-language-detection"></a>Microsoft 語言偵測

ELS 語言偵測服務稱為 Microsoft 語言偵測。 這項服務會使用 Microsoft 專利技術，讓應用程式能夠偵測撰寫特定文字的語言。

## <a name="input-to-microsoft-language-detection"></a>輸入至 Microsoft 語言偵測

Microsoft 語言偵測服務的輸入為 UTF-16 (正規化格式的 C) 文字。 服務必須判斷此文字的語言。

## <a name="output-of-microsoft-language-detection"></a>Microsoft 語言偵測的輸出

Microsoft 語言偵測服務會抓取雙值終止、登錄格式的 UTF-16 字串清單（以其名稱表示），並以 null 字元分隔符號分隔。 清單會依相關性排序。 針對大部分的語言，則會使用中性名稱。 不過，在某些情況下（例如，Cyrl、sr-iov Latn、zh Zh-hant 和 zh Hans），則會使用完整名稱。

## <a name="microsoft-language-detection-operation"></a>Microsoft 語言偵測操作

Microsoft 語言偵測服務會檢查應用程式所提供之文字的 Unicode 腳本。 它會根據所偵測到的腳本來分割文字，然後決定撰寫每個區段的語言。 如果腳本指出單一語言，語言的輸出清單中一定會有該語言。 此服務會使用專利演算法來判斷每個支援語言的相關性。

## <a name="microsoft-language-detection-guid"></a>Microsoft 語言偵測 GUID

Microsoft 語言偵測服務的 GUID 是在 Elssrvc 中宣告，如下列程式碼所示。


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於擴充的語言服務](about-extended-linguistic-services.md)
</dt> </dl>

 

 




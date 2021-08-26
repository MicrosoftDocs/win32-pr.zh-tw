---
description: Tablet PC 平臺支援數個 factoids，可用來增加辨識精確度。
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: 從版本1支援的 Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c24c192bcbda04be7ea25deb0c7b1cb7b392de57c43ce7a509e0ceaac31002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934348"
---
# <a name="supported-factoids-from-version-1"></a>從版本1支援的 Factoids

\[請注意，在第1版的 Microsoft Windows XP Tablet PC Edition 軟體發展工具組中所支援的 factoids 描述， (SDK) 仍受到辨識器的支援，但建議所有適用于拉丁腳本的新開發 (，) 使用[InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)列舉中所定義的值。\]

Tablet PC 平臺支援數個 factoids，可用來增加辨識精確度。 使用 factoids 時，預期的輸入必須完全符合模擬程式的定義。 如果輸入不符合模擬程式的定義，辨識精確度就會受到影響。 例如，如果設定了 **數位** 的智慧標籤，而使用者輸入字母，則字母的辨識精確度很差。

某些 factoids （例如 **電子郵件** 和 **數位**）幾乎在各語言之間都完全相同。 其他 factoids，例如 **電話** 和 **郵遞區號**，會因語言而異。 檢查您所使用之語言的每個模擬程式格式。 您可以在本主題後面主題的表格中，找到每個語言中每個模擬的格式清單。

> [!Note]  
> 西方語言的 factoids 與東亞語言的 factoids 有些許但重要的區別。 適用于西方語言的 Factoids 是使用描述所需結果的運算式來執行。 辨識器接著會產生偏差，以產生符合此運算式的結果。 適用于東亞語言的 Factoids 是藉由指定可接受的 Unicode 字元範圍來執行。 例如，適用于東亞語言的 **日期** 陳述，在特定範圍內只接受 Unicode 字元。

 

適用于西方語言的 Factoids 包含適用于英文的 Factoids (英國) 、英文 () 、法文、德文和西班牙文。 適用于東亞語言的 Factoids 包括 Factoids，適用于中文 (簡化) 、中文 (傳統) 、日文和韓文。

下列各節說明每種語言的每個模擬程式所支援的格式：

-   [跨語言的通用 Factoids](factoids-common-across-languages.md)
-   [適用于西方語言的 Factoids](factoids-for-western-languages.md)
-   [適用于東亞語言的 Factoids](factoids-for-east-asian-languages.md)

如果您預期輸入的輸入與這些章節的表格中所列的格式不同，請勿使用模擬。 此外，factoids 也內建于每種語言的辨識器中。 您無法從另一種語言的辨識器使用 factoids。 例如，您不能使用法文 **電話** 模擬的日文辨識器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**模擬常數**](factoid-constants.md)
</dt> <dt>

[Microsoft 墨水瓶類別](/previous-versions/ms583657(v=vs.100))
</dt> </dl>

 

 

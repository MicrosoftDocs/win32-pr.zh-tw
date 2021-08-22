---
description: ICE58 會檢查您的媒體資料表是否沒有超過80個數據列。
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0be8cec8fda3a3ddc1efce397dfbd17a95a2baf37ab0392eb8e5ffd08c7df4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528228"
---
# <a name="ice58"></a>ICE58

ICE58 會檢查您的 [媒體資料表](media-table.md) 是否沒有超過80個數據列。

## <a name="result"></a>結果

ICE58 回報的警告會導致安裝失敗，除非封裝是使用 Windows Installer 2.0 或更新版本安裝。 從 Windows Installer 2.0 開始，會移除超過80個媒體資料表專案的限制。 如果封裝的 [**頁面計數摘要**](page-count-summary.md) 屬性大於或等於150，則不會發出任何警告。 架構200或更高版本的套件只能由 Windows Installer 2.0 或更新版本安裝。

## <a name="example"></a>範例

ICE58 會針對所顯示的範例報告下列錯誤和警告。

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

若要修正這個錯誤，請排除任何未使用的媒體資料表專案、合併參考相同媒體的媒體資料表專案，以及重新封裝您的應用程式以減少所需的媒體。

[媒體資料表](media-table.md) (部分) 



| DiskId | LastSequence\_ |
|--------|----------------|
| 1      | 10             |
| 2      | 20             |
| ...    | ...            |
| 81     | 810            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




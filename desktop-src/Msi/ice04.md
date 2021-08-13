---
description: ICE04 會驗證檔案資料表中每個檔案的序號是否小於或等於媒體資料表 LastSequence 資料行中的最大序號。
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b77bf11d26d694a25f62db8da005139566b2c92310e2bb2dded4eecbca79719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635660"
---
# <a name="ice04"></a>ICE04

ICE04 會驗證檔案 [資料表](file-table.md) 中每個檔案的序號是否小於或等於 [媒體資料表](media-table.md)LastSequence 資料行中的最大序號。

媒體資料表中的每一筆記錄都代表來源媒體上的磁片，其中的序號小於或等於 LastSequence 資料行中的值，且大於前一個磁片記錄中的 LastSequence 值。

## <a name="result"></a>結果

如果有序號大於來源媒體的最大 LastSequence 數目的檔案，ICE04 會張貼錯誤訊息。

## <a name="example"></a>範例

ICE04 會針對所顯示的範例報告下列錯誤：

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

[檔資料表](file-table.md) (部分) 



| 檔案   | 順序 |
|--------|----------|
| Myfile.txt | 210      |



 

[媒體資料表](media-table.md) (部分) 



| DiskId | LastSequence |
|--------|--------------|
| 1      | 100          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




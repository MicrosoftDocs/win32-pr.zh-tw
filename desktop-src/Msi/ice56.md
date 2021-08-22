---
description: ICE56 會驗證 .msi 檔的目錄結構是否具有單一根目錄、根目錄是 TARGETDIR 屬性，以及 SourceDir 屬性值是否在目錄資料表的 DefaultDir 資料行中。
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c1feb3e3dbab84a58809496b28a60d3a2436c3041d3a2d58f0ac8f2b5e47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528218"
---
# <a name="ice56"></a>ICE56

ICE56 會驗證 .msi 檔的目錄結構是否具有單一根目錄、根目錄是 [**TARGETDIR**](targetdir.md) 屬性，以及 [**SourceDir**](sourcedir.md) 屬性值是否在 [目錄資料表](directory-table.md)的 DefaultDir 資料行中。

如果 .msi 檔案有多個根目錄或指定 [**TARGETDIR**](targetdir.md)以外的根目錄， [系統管理安裝](administrative-installation.md) 不會建立正確的系統管理映射。

請注意，ICE56 不會檢查空的目錄。 如果額外的目錄是空的，則目錄結構會以多個根目錄傳遞驗證。

## <a name="result"></a>結果

如果 .msi 沒有單一根、 [**TARGETDIR**](targetdir.md)，或 [目錄資料表](directory-table.md)的 DefaultDir 資料行中未指定 [**SourceDir**](sourcedir.md) ，ICE56 會張貼錯誤。

## <a name="example"></a>範例

ICE56 會針對所顯示的範例報告下列錯誤。

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[目錄資料表](directory-table.md)



| 目錄 | 目錄 \_ 父系 | DefaultDir |
|-----------|-------------------|------------|
| TARGETDIR |                   | Temp       |
| Root2     | Root2             | SourceDir  |



 

若要修正第一個錯誤， [**TARGETDIR**](targetdir.md) 根目錄應具有 [**SourceDir**](sourcedir.md)的 DefaultDir 值。 也接受 SOURCEDIR。 您可以將 **TARGETDIR** 設為第二個根節點的父系，並使用 DefaultDir 資料行中的 '. ' 值。 如需詳細資訊，請參閱 [目錄表格](directory-table.md) 。

為了修正第二個錯誤，目錄結構只能有一個稱為 [**TARGETDIR**](targetdir.md)的根目錄。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




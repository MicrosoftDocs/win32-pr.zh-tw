---
description: ICE76 會確認適用于 Windows Me Windows Installer 套件內的 SFP (WFP) 目錄。 這項 ICE 也會確認 BindImage 資料表中沒有任何檔案參考 SFP 目錄。
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972460"
---
# <a name="ice76"></a>ICE76

ICE76 會確認適用于 Windows Me Windows Installer 套件內的 SFP (WFP) 目錄。 這項 ICE 也會確認 BindImage [資料表](bindimage-table.md) 中沒有任何檔案參考 SFP 目錄。

Windows 檔案保護需要在類別目錄檔案中內嵌的檔案和簽章完全相符。 參考 SFP 類別目錄的檔案不能列在 BindImage 資料表中，因為這些檔案的 [BindImage 動作](bindimage-action.md) 效果與電腦之間的不同。 SFP 類別目錄所參考的檔案必須位於永久或本機安裝的元件中。

## <a name="result"></a>結果

ICE76 會將 [BindImage 資料表](bindimage-table.md) 中的每個檔案的錯誤張貼在 [FileSFPCatalog 資料表](filesfpcatalog-table.md)中。

如果 FileSFPCatalog 資料表中的檔案屬於下列任何 true 的元件，ICE76 會輸出錯誤：

-   **msidbComponentAttributesPermanent** 不會在 [元件資料表](component-table.md)的 [屬性] 資料行中設定。
-   **msidbComponentAttributesSourceOnly** 是在元件資料表的 [屬性] 資料行中設定。
-   **msidbAttributesOptional** 是在元件資料表的 [屬性] 資料行中設定。

## <a name="example"></a>範例

ICE76 會報告此範例的下列錯誤：

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

[FileSFPCatalog 資料表](filesfpcatalog-table.md) (部分) 



| 檔案\_ | SFPCatalog\_ |
|--------|--------------|
| File1  | Catalog1.Cat |



 

[BindImage 資料表](bindimage-table.md) (部分) 



| 檔案\_ |
|--------|
| File1  |



 

若要修正此問題，請不要在 BindImage 資料表中輸入參考 SFP 目錄的任何檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[BindImage 資料表](bindimage-table.md)
</dt> <dt>

[元件資料表](component-table.md)
</dt> <dt>

[FileSFPCatalog 資料表](filesfpcatalog-table.md)
</dt> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




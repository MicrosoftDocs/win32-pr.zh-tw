---
description: ICE99 會確認目錄資料表中未輸入的屬性名稱會重複保留給 Windows Installer 的公用或私用。
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25744243ad5de8adc6a88ebc09890eb006d94e929a56e469ce802ad67f9a230b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315268"
---
# <a name="ice99"></a>ICE99

ICE99 會確認[目錄](directory-table.md)資料表中未輸入的屬性名稱會重複保留給 Windows Installer 的公用或私用。

## <a name="result"></a>結果

ICE99 會張貼下列錯誤。



| ICE99 錯誤                                                                                                      | Description                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| 目錄名稱： \[ 1 與 \] 其中一個 MSI 公用屬性相同，而且可能會造成未預期的副作用。 | [目錄](directory-table.md)資料表的目錄資料行中的值會重複 Windows Installer 所保留的屬性名稱。 |



 

## <a name="example"></a>範例

ICE99 會報告此範例的下列錯誤：

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

[目錄](directory-table.md) (部分) 



| 目錄        | 目錄 \_ 父系 | DefaultDir |
|------------------|-------------------|------------|
| CustomActionData |                   |            |



 

若要修正此警告，您應該變更 CustomActionData 的名稱。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> <dt>

[目錄資料表](directory-table.md)
</dt> <dt>

[Windows Installer 3.0 及更早版本不支援](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 




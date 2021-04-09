---
description: ICE92 會確認沒有元件識別碼 GUID 的元件也不會指定為永久元件。
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849972"
---
# <a name="ice92"></a>ICE92

ICE92 會確認沒有元件識別碼 GUID 的元件也不會指定為永久元件。 這個 ICE 自訂動作會檢查 [元件資料表](component-table.md) 中是否有未在 [元件識別碼] 欄位中指定 [GUID](guid.md) 的元件，並確認 [屬性] 欄位中尚未設定 **msidbComponentAttributesPermanent** 旗標。 ICE92 也會確認沒有任何元件同時有 **msidbComponentAttributesPermanent** 和 **msidbComponentAttributesUninstallOnSupersedence** 屬性。

如果元件的資料行是 null，安裝程式就不會註冊元件，而且安裝程式無法移除或修復元件。

## <a name="result"></a>結果

ICE92 會張貼下列錯誤。



| ICE92 錯誤                                                          | Description                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 元件 ' \[ 1 \] ' 沒有任何元件，並標示為永久。 | 元件資料表中此元件的專案在 [元件] 資料行中具有 null，且在 [屬性] 資料行中具有 **msidbComponentAttributesPermanent** 。 |



 

ICE92 會張貼下列警告。



| ICE92 警告                                                                                                                                                           | Description                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 元件 ' \[ 1 \] ' 標示為永久和卸載取代。 因為元件是永久性的，所以會忽略取代取代屬性。 | [元件資料表](component-table.md)中此元件的專案同時指定了 **msidbComponentAttributesPermanent** 和 **msidbComponentAttributesUninstallOnSupersedence** 屬性。 |



 

## <a name="example"></a>範例

ICE92 會報告此範例的下列錯誤：

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

[元件資料表](component-table.md) (部分) 



| 元件  | ComponentId | 目錄\_ | 屬性 | KeyPath |
|------------|-------------|-------------|------------|---------|
| Component1 |             | DirectoryA  | 16         | >filea.docx   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




---
description: ICE53 會檢查登錄表中的專案，以將私人安裝程式資訊或原則值寫入系統登錄。
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2d1e661eb832439a9b4fde423e005dc4b3a0c3ca9b266045c0ddd04daa63f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635129"
---
# <a name="ice53"></a>ICE53

ICE53 會檢查登錄表中的專案，以將私人安裝程式資訊或原則值寫入系統登錄。

## <a name="result"></a>結果

如果登錄資料表指定將內部或原則資訊寫入登錄，ICE53 會張貼警告。

## <a name="example"></a>範例

ICE53 會針對所顯示的範例張貼下列警告。

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

登錄[表](registry-table.md) (部分) 



| 登錄             | Root         | 答案                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| Registry1<br/> | 1<br/> | **軟體** \\**原則** \\**Microsoft** \\**Windows** \\**安裝程式** \\**DisableRollback**<br/> |



 

登錄資料表資料列 ' Registry1 ' 會寫入登錄中的系統原則值，以影響所有封裝的安裝。 根據封裝，您可以藉由在 [屬性工作表](property-table.md)中設定 [**DISABLEROLLBACK**](-disablerollback.md)屬性，來停用此封裝的復原。 請參閱 [復原安裝](rollback-installation.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 





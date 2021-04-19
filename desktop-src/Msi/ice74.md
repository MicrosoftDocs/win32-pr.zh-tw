---
description: ICE74 會確認 FASTOEM 屬性尚未撰寫至屬性資料表。
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974322"
---
# <a name="ice74"></a>ICE74

ICE74 會確認 [**FASTOEM**](fastoem.md) 屬性尚未撰寫至 [屬性資料表](property-table.md)。

[**FASTOEM**](fastoem.md)屬性可讓 oem 縮短第一次安裝 Windows Installer 應用程式所需的時間。 它無法在第一次安裝之後使用。 **FASTOEM** 屬性不能在屬性工作表中撰寫，因為這會干擾應用程式的維護、移除或修復後續安裝。

ICE74 也會確認 [**UpgradeCode**](upgradecode.md) 屬性已撰寫至 [屬性工作表](property-table.md)，而且其值不是 null GUID {00000000-0000-0000-0000-000000000000} 。

## <a name="result"></a>結果

ICE74 可以張貼下列錯誤。



| ICE74 錯誤                                                                       | Description                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**FASTOEM**](fastoem.md)屬性無法在屬性工作表中撰寫。 | 已在屬性工作表中設定 [**FASTOEM**](fastoem.md) 屬性。                             |
| ' \[ 2 \] ' 不是有效的 [**UpgradeCode**](upgradecode.md)。                        | 在屬性資料表中， [**UpgradeCode**](upgradecode.md) 屬性已輸入 null GUID。 |



 

ICE74 可以張貼下列警告。



| ICE74 警告                                                                                                                                                                                             | Description                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**UpgradeCode**](upgradecode.md)屬性不是在屬性工作表中撰寫的。 強烈建議安裝套件的作者為其應用程式指定 **UpgradeCode** 。 | [**UpgradeCode**](upgradecode.md)屬性不是在屬性工作表中撰寫的。 |



 

## <a name="example"></a>範例

如果設定 [**FASTOEM**](fastoem.md) 屬性，ICE74 會報告下列錯誤： FASTOEM

``` syntax
 property cannot be authored in the Property table.
```

[屬性工作表](property-table.md) (部分) 



| 屬性                   | 值 |
|----------------------------|-------|
| [**FASTOEM**](fastoem.md) | 1     |



 

若要修正這個錯誤，請從屬性資料表中移除 [**FASTOEM**](fastoem.md) 屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**FASTOEM 屬性**](fastoem.md)
</dt> <dt>

[屬性工作表](property-table.md)
</dt> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




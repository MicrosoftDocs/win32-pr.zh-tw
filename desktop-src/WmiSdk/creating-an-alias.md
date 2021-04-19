---
description: WMI 中的別名是類別或類別實例中，位於受控物件格式 (MOF) 檔中其他位置的符號參考。
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: 建立 WMI 別名
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975031"
---
# <a name="creating-a-wmi-alias"></a>建立 WMI 別名

WMI 中的 [*別名*](gloss-a.md) 是類別或類別實例中，位於受控物件格式 (MOF) 檔中其他位置的符號參考。 MOF 編譯器會使用別名來建立類別和實例之間的參考。 編譯器會將別名解析為它們所參考的類別，因此別名名稱無法在已編譯的程式碼中使用。 因此，用戶端應用程式無法使用別名來參考類別。

> [!Note]  
> WMI 支援向前參考，但不支援迴圈別名。

 

別名的範圍僅限於您在其中宣告別名的 MOF 檔案內。 因此，您通常會使用別名作為較長物件路徑的快捷方式。

**若要定義別名**

1.  將 "as $*aliasname*" 片語新增至實例或類別宣告。
2.  別名名稱會遵循與實例和類別名稱相同的規則，但別名名稱的開頭必須是貨幣符號 ($) 。 底線可出現在初始字元之後的別名名稱中。

下列程式碼範例說明如何在類別定義中使用別名。

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

下列程式碼範例說明如何使用別名做為物件路徑的符號參考。 這些範例會宣告兩個類別來描述磁片： Disk 類別指出磁碟機號，而 DiskRef 類別指出磁片路徑。 系統會為磁片類別實例定義別名。 此別名會當做 DiskRef 實例中 PathToDisk 屬性的值使用。

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立類別](creating-a-class.md)
</dt> </dl>

 

 




---
description: 您必須編譯主要 MOF 檔案，以建立語言中性和特定語言的 MOF 檔案。
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: 編譯當地語系化的 MOF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ab1341a37269ba98fdbbdecaa64b5e5a119703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319683"
---
# <a name="compiling-localized-mof-files"></a>編譯當地語系化的 MOF 檔案

您必須編譯主要 MOF 檔案，以建立語言中性和特定語言的 MOF 檔案。

在命令提示字元中輸入下列命令，以編譯主要 MOF 檔案。

**mofcomp.exe-MOF： Lnmof MFL： Lsmof. MFL-修訂： MS \_ 409 Mastermof. MOF**

當您執行此命令時，MOF 編譯器會從原始的 Mastermof mof 檔案建立兩個 MOF 檔案。 MOF 編譯器會產生語言中性版本 Lnmof，其中所有語言特定專案都會被移除。 此外，也會建立第二個語言特定版本 Lsmof。此檔案僅包含在 Mastermof 中以 [**修改**](qualifier-flavors.md) 過的限定詞類別標記的專案。

下列程式碼範例會顯示所產生的語言中性 MOF 檔案 (Lnmof) 的內容。

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

下列程式碼範例會顯示所產生之特定語言 MOF 檔案 (Lsmof mfl) 的內容。

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

使用 [**修改**](qualifier-flavors.md) 過的辨識符號編譯 MOF 檔案，只會產生不同的語言中性和特定語言的 mof 檔案;CIM 存放庫未更新為新的類別資訊。 您必須使用 MOF 編譯器來編譯兩個 MOF 檔案，這些檔案是在任何類別資訊可供 WMI 使用之前所產生的第一次編譯。

當您編譯主要 MOF 檔案時，只有已 [**修改**](qualifier-flavors.md) 之類別的限定詞會移至特定語言的 MOF 檔案。 沒有 **修改** 過之類別的限定詞不會當地語系化，而且只存在於語言中立的 MOF 檔案中的基本類別定義中。 如果未提供當地語系化的說明，則可使用未當地語系化的限定詞作為預設描述。

您可以使用 [pragma 修訂](pragma-amendment.md) 命令，而不是指定 [**修改**](qualifier-flavors.md) 為 MOF 編譯器的參數。 其中一個選項相當於要求特定語言和語言中性版本的 MOF 檔案。 如果您使用 pragma 修訂命令或 **修改** 過的命令列選項，您必須在命令提示字元中使用 **-MFL** 和 **-MOF** 選項來指定輸出檔的名稱。

> [!Note]  
> MOF 編譯器所產生的非語言相關 MOF 檔案包含地區設定識別碼的十進位對等專案，即使以十六進位輸入此值也是如此。 在上述範例中，編譯器已將 Lnmof mof 輸出檔的值0x409 轉換為十進位數1033。

 

 

 




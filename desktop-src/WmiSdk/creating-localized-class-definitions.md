---
description: 建立當地語系化的類別定義是三個步驟的處理常式。
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: 建立當地語系化的類別定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41a183c1478c259b0428cd827088a769e680425
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106976638"
---
# <a name="creating-localized-class-definitions"></a>建立當地語系化的類別定義

建立當地語系化的類別定義是三個步驟的處理常式。 首先，撰寫定義類別的 MOF 程式碼，包括必須當地語系化的所有限定詞。 此原始檔案稱為「主要 MOF」檔案，因為它包含定義類別的所有限定詞和屬性。

接下來，使用 [mof 編譯器](mofcomp.md) 來建立特定語言和特定語言版本的 MOF 檔案。 MOF 編譯器會將基本類別描述放置在新的 MOF 檔案中，並建立 MOF 檔案的當地語系化版本，其中只包含必須當地語系化的屬性和限定詞。 雖然 MOF 檔案的語言特定和語言中性版本可以有相同的檔案名，但您應該使用 mfl 副檔名來指出檔案包含當地語系化的資訊。 如有必要，您可以將 mfl 檔案當地語系化為其他地區設定。 將類別定義儲存在 CIM 存放庫中，需要額外的步驟來使用 MOF 編譯器，以編譯非語言相關和語言專屬的 MOF 檔案。

下列步驟說明如何建立和儲存當地語系化的類別定義。

**若要建立和儲存當地語系化的類別定義**

1.  建立主要 MOF 檔案，以定義您要當地語系化的類別。

    將此 MOF 程式碼儲存在名為 Mastermof 的檔案中。

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
    {
        [DisplayName("User Name") : Amended,
        Description("The Name property contains the name of the user") : 
        Amended, key]
         string Name;

        uint64 Value; // non-localized value field

          [DisplayName("Time Stamp") : Amended,
        Description("This property shows when the object was created") : 
        Amended] 
         uint64 Timestamp;
    };
    ```

2.  藉由編譯 MasterMOF mof 檔案，建立特定語言和特定語言版本的 MOF 檔案。

    在命令提示字元中輸入下列命令，以編譯 MasterMOF mof 檔案。

    **mofcomp.exe-MOF： Lnmof MFL： Lsmof. MFL-修訂： MS \_ 409 Mastermof. MOF**

3.  編譯語言中立的 (Lnmof mof) 和特定語言的 (Lsmof mfl) 檔，並將類別資訊儲存在 CIM 存放庫中。

    在命令提示字元中輸入下列命令，將類別資訊儲存在 CIM 存放庫中。

    **Mofcomp.exe Lnmof**

    **Mofcomp.exe Lsmof. mfl**

    編譯這些檔案之後，根測試命名空間中將會有語言中立的類別定義 \\ ，以及根 \\ 測試 \\ ms \_ 409 命名空間中的當地語系化類別定義。 如需編譯當地語系化 MOF 檔案的詳細資訊，請參閱 [編譯當地語系化的 mof](compiling-localized-mof-files.md)檔案。

 

 




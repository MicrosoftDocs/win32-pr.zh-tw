---
description: 您可以使用部分值對應來當地語系化靜態屬性。
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: 將靜態屬性當地語系化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c51999c68a05e8d7b8cf3fd8c5218bc171931303d86a50c04f32c5d80efb308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050726"
---
# <a name="localizing-static-properties"></a>將靜態屬性當地語系化

您可以使用部分值對應來當地語系化靜態屬性。

下列程式描述如何搭配使用部分值對應與正則運算式來當地語系化靜態屬性。

**使用值對應將靜態屬性當地語系化**

1.  建立 (Mastervm mof) 的主要 MOF 檔案。

    下列程式碼範例可用來建立 (Mastervm mof) 的主要 MOF 檔案。

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  建立 MOF 檔案的語言中性和語言特定版本。

    在命令提示字元中輸入下列命令，以建立特定語言和特定語言版本的 MOF 檔案。

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    MOF 編譯器會產生語言特定和語言中性的 MOF 檔案，LnVm. MOF 和 LsVm mfl。 [ [數位](numbers.md) ] 屬性的美式英文值會放在美式英文命名空間的 mfl 檔案中。

    下列程式碼範例顯示 LsVm mfl 檔案的內容。

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  編譯兩個 MOF 檔案，並將類別資訊儲存在 CIM 存放庫中。

    在命令提示字元中輸入下列命令，以編譯兩個 MOF 檔案。

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  當地語系化其他地區設定的 MFL 檔案。

    下列程式碼範例會顯示法文命名空間之 MFL 檔的內容。

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

最後的結果是，[ [數位](numbers.md) ] 屬性的顯示名稱和值都取決於已登入使用者的地區設定。 如果使用者指定了尚未提供的地區設定，則預設的辨識符號資料會來自英文 (ms \_ 409) 命名空間。

這項設計的含意是，每個字串值都是用來做為無法當地語系化的查閱識別碼。 定義此配置時，您必須確定提供者所放置的值與地區設定無關。

> [!Note]  
> WMI 目前未提供將值對應至由限定詞所定義之字串的執行時間支援。 建議語法的解讀是應用程式的責任。

 

 

 




---
description: 存取未命名的登錄值
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: 存取未命名的登錄值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975469"
---
# <a name="accessing-an-unnamed-registry-value"></a>存取未命名的登錄值

登錄機碼的預設值或未命名值，會顯示為 (預設) 或 <No Name> 在 Regedit 登錄編輯程式中。 您可以使用系統登錄提供者來存取未命名的登錄機碼。 同樣地，您也可以使用系統登錄提供者來存取點陣圖描述（定義為未命名值）。

下列程式描述如何取出未命名的登錄值。

**取出未命名的登錄值**

1.  定義屬性，並將該屬性的 **PropertyCoNtext** 限定詞設定為空字串。

    下列程式碼範例會示範類別如何定義屬性來保存 **ClassCoNtext** 限定詞所指定之索引鍵的值。 預設值會儲存在 **預設** 屬性中。

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    傳輸索引鍵不會使用未命名的值，因此除非使用登錄編輯工具來變更未命名的值，否則此 MOF 檔案的編譯不會產生任何 **預設** 屬性的值。

2.  若為點陣圖檔案，請定義屬性，並設定該屬性的 **PropertyCoNtext** 。

    下列程式碼範例顯示如何定義屬性。

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 




---
description: 西歐語言的定義為英文 (英國) 、英文 (美國) 、法文、德文和西班牙文。
ms.assetid: d4728506-7484-4c4c-a5ae-e98d699f7e76
title: 適用于西方語言的 Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de98cfce0203a2a3a94509d6586c1596390ca16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026261"
---
# <a name="factoids-for-western-languages"></a>適用于西方語言的 Factoids

西歐語言的定義為英文 (英國) 、英文 (美國) 、法文、德文和西班牙文。 下表所示的每個模擬程式中的格式，都是每個語言的辨識器所特有。 例如，每種語言的 **電話** 模擬程式都不同。 此外，每個模擬程式都有特定的辨識器。 例如，法文 **電話** 模擬程式只能搭配法文辨識器使用。

> [!Note]  
> 除了下列 factoids 之外，所有語言都會使用 [Factoids 通用](factoids-common-across-languages.md)的 factoids。

 



| 標記              | 定義                                                                                                                                                                                                                                                                                                                                                                                                           | 範例                                                                                                                                                                                                                                                            |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **檔案名稱**         | 設定檔案名路徑的偏差。 名稱不能包含字元<br/> /" < > \|<br/> 字元 \* 和？ 包含在此模擬中，以啟用搜尋功能。 此外，歐洲語言支援擴充的字元。<br/>                                                                                                                                                    | c:<br/> \\\\directoryname \\ 檔案名<br/> \\\\directory1 \\ directory2 \\ 檔案名<br/> \\\\directoryname \\ \* 。\*<br/> 檔案名。？<br/> myfile.doc<br/>                                                                                |
| **SystemDictionary** | 只啟用系統字典。 如果應用程式會查詢單字是否在系統字典中，這會很有用。 將模擬設定為 **SystemDictionary** 並呼叫 [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) 方法。<br/>                                                                                                                                                 | 預設語言模型包含語言和系統字典的文法。 這項模擬程式會將辨識僅偏差在系統字典中所發生的單字。 每種語言都有自己的系統字典。<br/>                   |
| **單詞表**         | 只啟用單字清單。 如果將此模擬設定為 **單詞表** ，但是未在 managed 程式碼) 中將任何字組指派給 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) ([RecognizerCoNtext](/previous-versions/ms552546(v=vs.100)) ，則會使用該使用者字典。 如需有關 word 清單和字典的詳細資訊，請參閱 [使用應用程式字典](using-application-dictionaries.md)。<br/> | 此模擬器會將辨識器偏移，使其只傳回單字清單中的單字。 例如，若要讓使用者在表單中輸入色彩，您可以使用此模擬，以及包含 "綠"、"Red"、"Blue"、"白色" 和其他色彩的單字清單。<br/> |



 

下列 factoids 組合僅支援西方語言。  (Api) 的這一版 Tablet PC 平臺應用程式開發介面不支援其他 factoids 組合。 這些模擬組合使用邏輯 **OR** 運算子，因此輸入可以符合運算式中的任何 factoids。



| 模擬組合     | 定義                                                                   |
|-------------------------|------------------------------------------------------------------------------|
| **WebWordList**         | **Web** 模擬或字組清單。<br/>                             |
| **EmailWordList**       | **電子郵件** 的智慧標籤或字組清單。<br/>                           |
| **FilenameWebWordList** | **檔案名** 模擬或 **Web** 模擬或字組清單。<br/> |



 

下列主題顯示每種西方語言支援的格式。

-   [英文 (全球) Factoids](english--worldwide--factoids.md)
-   [英文 (美國) Factoids](english--united-states--factoids.md)
-   [法文 Factoids](french-factoids.md)
-   [德文 Factoids](german-factoids.md)
-   [西班牙文 Factoids](spanish-factoids.md)

 


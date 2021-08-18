---
description: 將一個 MOF 檔案的內容包含在另一個 MOF 檔案中。
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b7577639bd215fc051c2f1303e74fe946341a31c4b6708f881c3c9fabae2372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557774"
---
# <a name="include"></a>' #include '
/* 標題： MyMof。 Mof                           *//*   標題： MyMof2

\#包含預處理器命令會將一個 mof 檔案的內容包含在另一個 mof 檔案中。 下列程式碼範例描述 include 命令的語法 \# 。

``` syntax
#include ("Moffile.mof")
```

在上述範例中，Moffile 是要包含的 MOF 檔案名。

下列範例顯示兩個 MOF 檔案。 當您編譯第一個 MOF 檔案時，編譯器會在您放置 include 語句的位置中，自動編譯第二個 MOF 檔案 (Mymof2) 。 \#

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

上述範例包含下列 MOF 檔案：

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預處理器命令](preprocessor-commands.md)
</dt> </dl>

 

 




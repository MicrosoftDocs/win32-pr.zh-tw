---
description: 建立命名空間的另一種方式是使用受控物件格式 (MOF) 程式碼來建立同級命名空間。 同一個命名空間是指不是目前命名空間子系的命名空間。
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: 使用 MOF 程式碼建立同級命名空間
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4fcbf6e16ad51ab9a0df63e3497735b07cd6afc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998331"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a>使用 MOF 程式碼建立同級命名空間

建立命名空間的另一種方式是使用受控物件格式 (MOF) 程式碼來建立同級命名空間。 同一個命名空間是指不是目前命名空間子系的命名空間。

下列程式描述如何使用 MOF 程式碼建立同級命名空間。

**使用 MOF 程式碼建立同級命名空間**

1.  在命名空間宣告之前，將 [**\# pragma namespace**](pragma-namespace.md)命令插入您的 MOF 程式碼。

    [**\# Pragma namespace**](pragma-namespace.md)命令會指示 WMI 在指示詞之後建立實例的位置。

2.  建立 [**\_ \_ 命名空間**](--namespace.md)類別的實例。
3.  使用 [mofcomp.exe](mofcomp.md) 公用程式或 [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 介面編譯您的程式碼。

    如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

下列 MOF 程式碼範例說明如何將命名空間建立為 "Root \\ CIMv2" 命名空間的同級。

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 




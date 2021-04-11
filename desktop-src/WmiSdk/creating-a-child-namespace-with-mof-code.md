---
description: 建立命名空間最簡單的方式，就是使用受控物件格式 (MOF) 程式碼，在目前的目錄中建立命名空間。 當您登入時，會定義目前的目錄。
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: 使用 MOF 程式碼建立子命名空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80aa04e2ef4f5c7bbfc43d9020727b3b2a6e0d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104027692"
---
# <a name="creating-a-child-namespace-with-mof-code"></a>使用 MOF 程式碼建立子命名空間

建立命名空間最簡單的方式，就是使用受控物件格式 (MOF) 程式碼，在目前的目錄中建立命名空間。 當您登入時，會定義目前的目錄。

下列程式說明如何使用 MOF 程式碼建立子命名空間。

**使用 MOF 程式碼建立子命名空間**

1.  建立 [**\_ \_ 命名空間**](--namespace.md)類別的實例。

    下列程式碼範例顯示如何建立子命名空間。

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  如果您想要要求使用者對命名空間進行加密的連接，請使用 **RequiresEncryption** 限定詞。 如需詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。

    下列程式碼範例示範如何要求加密的連接。

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  如果您想要在命名空間上設定安全描述項，而不是使用預設的命名空間安全性，請使用 **NamespaceSecuritySDDL** 限定詞。 如需詳細資訊，請參閱 [在建立命名空間時設定命名空間安全性](setting-namespace-security-when-the-namespace-is-created.md)。

    下列程式碼範例顯示如何在命名空間上設定安全描述項。

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  使用 [mofcomp.exe](mofcomp.md)公用程式或 [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)介面，編譯和載入 [**\_ \_ 命名空間**](--namespace.md)實例。 Mofcomp.exe 和 **IMofCompiler** 介面都會將命名空間自動載入至目前的目錄。 如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**標準 WMI 限定詞**](standard-wmi-qualifiers.md)
</dt> </dl>

 

 




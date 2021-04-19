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
# <a name="creating-a-sibling-namespace-with-mof-code"></a><span data-ttu-id="a7072-104">使用 MOF 程式碼建立同級命名空間</span><span class="sxs-lookup"><span data-stu-id="a7072-104">Creating a Sibling Namespace with MOF Code</span></span>

<span data-ttu-id="a7072-105">建立命名空間的另一種方式是使用受控物件格式 (MOF) 程式碼來建立同級命名空間。</span><span class="sxs-lookup"><span data-stu-id="a7072-105">Another way of creating a namespace is to use Managed Object Format (MOF) code to create a sibling namespace.</span></span> <span data-ttu-id="a7072-106">同一個命名空間是指不是目前命名空間子系的命名空間。</span><span class="sxs-lookup"><span data-stu-id="a7072-106">A sibling namespace is a namespace that does not exist as a child of the current namespace.</span></span>

<span data-ttu-id="a7072-107">下列程式描述如何使用 MOF 程式碼建立同級命名空間。</span><span class="sxs-lookup"><span data-stu-id="a7072-107">The following procedure describes how to create a sibling namespace with MOF code.</span></span>

<span data-ttu-id="a7072-108">**使用 MOF 程式碼建立同級命名空間**</span><span class="sxs-lookup"><span data-stu-id="a7072-108">**To create a sibling namespace with MOF code**</span></span>

1.  <span data-ttu-id="a7072-109">在命名空間宣告之前，將 [**\# pragma namespace**](pragma-namespace.md)命令插入您的 MOF 程式碼。</span><span class="sxs-lookup"><span data-stu-id="a7072-109">Insert the [**\#pragma namespace**](pragma-namespace.md) command into your MOF code prior to the namespace declaration.</span></span>

    <span data-ttu-id="a7072-110">[**\# Pragma namespace**](pragma-namespace.md)命令會指示 WMI 在指示詞之後建立實例的位置。</span><span class="sxs-lookup"><span data-stu-id="a7072-110">The [**\#pragma namespace**](pragma-namespace.md) command instructs WMI where to create the instances following the directive.</span></span>

2.  <span data-ttu-id="a7072-111">建立 [**\_ \_ 命名空間**](--namespace.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a7072-111">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>
3.  <span data-ttu-id="a7072-112">使用 [mofcomp.exe](mofcomp.md) 公用程式或 [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 介面編譯您的程式碼。</span><span class="sxs-lookup"><span data-stu-id="a7072-112">Compile your code with the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="a7072-113">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="a7072-113">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="a7072-114">下列 MOF 程式碼範例說明如何將命名空間建立為 "Root \\ CIMv2" 命名空間的同級。</span><span class="sxs-lookup"><span data-stu-id="a7072-114">The following MOF code example describes how to create a namespace as a sibling to the "Root\\CIMv2" namespace.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 




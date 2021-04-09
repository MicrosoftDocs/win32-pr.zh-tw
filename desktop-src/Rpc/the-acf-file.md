---
title: ACF 檔案
description: ACF 檔案可讓您自訂用戶端和/或伺服器應用程式的 RPC 介面，而不會影響介面的網路特性。
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933568"
---
# <a name="the-acf-file"></a><span data-ttu-id="fe5c1-103">ACF 檔案</span><span class="sxs-lookup"><span data-stu-id="fe5c1-103">The ACF File</span></span>

<span data-ttu-id="fe5c1-104">ACF 檔案可讓您自訂用戶端和/或伺服器應用程式的 RPC 介面，而不會影響介面的網路特性。</span><span class="sxs-lookup"><span data-stu-id="fe5c1-104">The ACF file enables you to customize your client and/or server applications' RPC interface without affecting the network characteristics of the interface.</span></span> <span data-ttu-id="fe5c1-105">例如，如果您的用戶端應用程式包含只在本機電腦上具有意義的複雜資料結構，您可以在 ACF 檔案中指定該結構中的資料如何以與電腦無關的形式表示，以進行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="fe5c1-105">For example, if your client application contains a complex data structure that only has meaning on the local machine, you can specify in the ACF file how the data in that structure can be represented in a machine-independent form for remote procedure calls.</span></span>

<span data-ttu-id="fe5c1-106">本教學課程示範 ACF 檔的另一個用法—指定代表用戶端與伺服器之間連接的系結控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="fe5c1-106">This tutorial demonstrates another use of the ACF file—specifying the type of binding handle that represents the connection between client and server.</span></span> <span data-ttu-id="fe5c1-107">**\[** ACF 標頭中的 [**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle) **\]** 屬性，可讓用戶端應用程式選取伺服器進行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="fe5c1-107">The **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]** attribute in the ACF header allows the client application to select a server for its remote procedure call.</span></span> <span data-ttu-id="fe5c1-108">ACF 會將 (MIDL 基本資料類型) 的控制碼定義為類型 [**控制碼 \_ t**](/windows/desktop/Midl/handle-t) 。</span><span class="sxs-lookup"><span data-stu-id="fe5c1-108">The ACF defines the handle to be of the type [**handle\_t**](/windows/desktop/Midl/handle-t) (a MIDL primitive data type).</span></span> <span data-ttu-id="fe5c1-109">MIDL 編譯器會將 ACF 指定的系結控制碼名稱，hello \_ IfHandle 到它所產生的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="fe5c1-109">The MIDL compiler will put the binding handle name that the ACF specified, hello\_IfHandle into the header file it generates.</span></span> <span data-ttu-id="fe5c1-110">請注意，這個特定的 ACF 檔有空白主體。</span><span class="sxs-lookup"><span data-stu-id="fe5c1-110">Notice that this particular ACF file has an empty body.</span></span>

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

<span data-ttu-id="fe5c1-111">MIDL 編譯器有一個選項 [**/app \_ config**](/windows/desktop/Midl/-app-config)，可讓您在 IDL 檔案中包含某些 ACF 屬性，例如 **隱含 \_ 控制碼**，而不是建立個別的 ACF 檔案。</span><span class="sxs-lookup"><span data-stu-id="fe5c1-111">The MIDL compiler has an option, [**/app\_config**](/windows/desktop/Midl/-app-config), that lets you include certain ACF attributes, such as **implicit\_handle**, in the IDL file, rather than creating a separate ACF file.</span></span> <span data-ttu-id="fe5c1-112">如果您的應用程式不需要太多特殊設定，且嚴格憑證相容性不是問題，請考慮使用此選項。</span><span class="sxs-lookup"><span data-stu-id="fe5c1-112">Consider using this option if your application doesn't require a lot of special configuration and if strict OSF compatibility is not an issue.</span></span>

 

 
---
title: IDL 檔案
description: IDL 檔案包含一或多個介面定義，其中每個都有標頭和主體。
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862adfad2a43f10dac3598279554fd6e1f00a302
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463233"
---
# <a name="the-idl-file"></a><span data-ttu-id="96162-103">IDL 檔案</span><span class="sxs-lookup"><span data-stu-id="96162-103">The IDL File</span></span>

<span data-ttu-id="96162-104">IDL 檔案包含一或多個介面定義，其中每個都有標頭和主體。</span><span class="sxs-lookup"><span data-stu-id="96162-104">The IDL file consists of one or more interface definitions, each of which has a header and a body.</span></span> <span data-ttu-id="96162-105">標頭包含適用于整個介面的資訊，例如 UUID。</span><span class="sxs-lookup"><span data-stu-id="96162-105">The header contains information that applies to the entire interface, such as the UUID.</span></span> <span data-ttu-id="96162-106">這項資訊會以方括弧括住，後面接著關鍵字 **介面** 和介面名稱。</span><span class="sxs-lookup"><span data-stu-id="96162-106">This information is enclosed in square brackets and is followed by the keyword **interface** and the interface name.</span></span> <span data-ttu-id="96162-107">本文包含 C 樣式的資料類型定義和函式原型，並以描述如何透過網路傳輸資料的屬性來擴充。</span><span class="sxs-lookup"><span data-stu-id="96162-107">The body contains C-style data type definitions and function prototypes, augmented with attributes that describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="96162-108">在此範例中，介面標頭只包含 UUID 和版本號碼。</span><span class="sxs-lookup"><span data-stu-id="96162-108">In this example, the interface header contains only the UUID and the version number.</span></span> <span data-ttu-id="96162-109">版本號碼可確保在有多個版本的 RPC 介面時，只會連接相容的用戶端和伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="96162-109">The version number ensures that when there are multiple versions of an RPC interface, only compatible versions of the client and server will be connected.</span></span>

<span data-ttu-id="96162-110">介面主體包含 **HelloProc** 的函式原型。</span><span class="sxs-lookup"><span data-stu-id="96162-110">The interface body contains the function prototype for **HelloProc**.</span></span> <span data-ttu-id="96162-111">在此原型中，函數參數 pszString 具有 **\[** [](/windows/desktop/Midl/in) **\]** 和 **\[** [**字串**](/windows/desktop/Midl/string)中的屬性 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="96162-111">In this prototype, the function parameter pszString has the attributes **\[**[**in**](/windows/desktop/Midl/in)**\]** and **\[**[**string**](/windows/desktop/Midl/string)**\]**.</span></span> <span data-ttu-id="96162-112">**\[ In \]** 屬性會告知執行時間程式庫，參數只會從用戶端傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="96162-112">The **\[in\]** attribute tells the run-time library that the parameter is passed only from the client to the server.</span></span> <span data-ttu-id="96162-113">**\[ 字串 \]** 屬性會指定存根應將參數視為 C 樣式字元字串。</span><span class="sxs-lookup"><span data-stu-id="96162-113">The **\[string\]** attribute specifies that the stub should treat the parameter as a C-style character string.</span></span>

<span data-ttu-id="96162-114">用戶端應用程式應該能夠關閉伺服器應用程式，因此介面會包含另一個遠端函式 **關閉** 的原型，稍後在本教學課程中將會執行此程式。</span><span class="sxs-lookup"><span data-stu-id="96162-114">The client application should be able to shut down the server application, so the interface contains a prototype for another remote function,**Shutdown** , that will be implemented later in this tutorial.</span></span>

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 
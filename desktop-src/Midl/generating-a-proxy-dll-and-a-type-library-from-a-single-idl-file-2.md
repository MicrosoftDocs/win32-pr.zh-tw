---
title: 從單一 IDL 檔案產生 Proxy DLL 和型別程式庫
description: 您可以使用單一 IDL 檔案，為封送處理常式代碼和類型程式庫產生 proxy stub 和標頭檔。
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Microsoft 介面定義語言 MIDL、工作、產生 proxy DLL 和型別程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81001bba7aeff416e765291d3e6660b705919a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021822"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a><span data-ttu-id="ae61f-104">從單一 IDL 檔案產生 Proxy DLL 和型別程式庫</span><span class="sxs-lookup"><span data-stu-id="ae61f-104">Generating a Proxy DLL and a Type Library from a Single IDL File</span></span>

<span data-ttu-id="ae61f-105">您可以使用單一 IDL 檔案，為封送處理常式代碼和類型程式庫產生 proxy stub 和標頭檔。</span><span class="sxs-lookup"><span data-stu-id="ae61f-105">You can use a single IDL file to generate both the proxy stubs and header files for marshaling code, and a type library.</span></span> <span data-ttu-id="ae61f-106">做法是在程式庫區塊之外定義介面，然後從程式庫區塊內部參考該介面，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="ae61f-106">You do this by defining an interface outside the library block and then referencing that interface from inside the library block, as shown in this example:</span></span>

``` syntax
//file: AllKnown.idl

[
    object, uuid(. . .), <other interface attributes>
]
interface IKnown : IUnknown 
{
    import "unknwn.idl";
    <declarations, etc. for IKnown interface go here>
};

[
    <library attributes>
]
library KnownLibrary 
{

    //reference interface IKnown:
    interface IKnown;

    //or create a new class:
    [
        <coclass attributes>
    ] 
    coclass KnowMore 
    {
       interface IKnown;
    };
};
```

<span data-ttu-id="ae61f-107">如需詳細資訊，請參閱 [封送處理 OLE 資料類型](marshaling-ole-data-types.md) 和 [產生類型程式庫所需的其他](additional-files-required-to-generate-a-type-library-2.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="ae61f-107">For more information, see [Marshaling OLE Data Types](marshaling-ole-data-types.md) and [Additional Files Required To Generate a Type Library](additional-files-required-to-generate-a-type-library-2.md).</span></span>

 

 





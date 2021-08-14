---
title: 從單一 IDL 檔案產生 Proxy DLL 和型別程式庫
description: 您可以使用單一 IDL 檔案，為封送處理常式代碼和類型程式庫產生 proxy stub 和標頭檔。
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Microsoft 介面定義語言 MIDL、工作、產生 proxy DLL 和型別程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e7bf2694b791007b0f1da303525217cf55d75d574e083c6d1756bc2784d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384234"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a>從單一 IDL 檔案產生 Proxy DLL 和型別程式庫

您可以使用單一 IDL 檔案，為封送處理常式代碼和類型程式庫產生 proxy stub 和標頭檔。 做法是在程式庫區塊之外定義介面，然後從程式庫區塊內部參考該介面，如下列範例所示：

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

如需詳細資訊，請參閱 [封送處理 OLE 資料類型](marshaling-ole-data-types.md) 和 [產生類型程式庫所需的其他](additional-files-required-to-generate-a-type-library-2.md)檔案。

 

 





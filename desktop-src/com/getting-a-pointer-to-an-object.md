---
title: 取得物件的指標
description: 取得物件的指標
ms.assetid: 4af9d356-402b-4e69-9f6e-8589057d3ac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc588518d5c3da884755d7db122738ca2fca257d76a1f8219867da357ef8444f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736697"
---
# <a name="getting-a-pointer-to-an-object"></a>取得物件的指標

因為 COM 沒有嚴格的類別模型，所以用戶端有四種方式可以具現化或取得物件介面的指標：

-   呼叫 COM 程式庫函式，此函式會建立預先決定之類型的物件。也就是說，函式只會傳回特定物件類別的一個特定介面指標。
-   呼叫 COM 程式庫函式，此函式可以根據類別識別碼 (CLSID) 來建立物件，並傳回所要求的任何介面指標類型。
-   呼叫某些介面的方法，以建立另一個物件 (或連接到現有的物件) 並傳回該個別物件上的介面指標。
-   使用介面來執行物件，讓其他物件將其介面指標直接傳遞給用戶端。

如需取得第一個物件之後，在物件上取得其他介面之指標的詳細資訊，請參閱 [QueryInterface：在物件中導覽](queryinterface--navigating-in-an-object.md)。

## <a name="creating-an-object-of-a-predetermined-type"></a>建立預先決定類型的物件

有許多 COM 函式（例如 [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc)）會傳回特定介面實的指標。  (**CoGetMalloc** 會抓取標準 COM 記憶體配置器的指標。 ) 這些都是協助程式函式，且大部分的函式會在相關的特定區域（例如儲存體或資料傳輸）下，在本檔的參考區段中加以描述。

## <a name="creating-an-object-based-on-a-clsid"></a>根據 CLSID 建立物件

有幾個函式（假設有 CLSID），用戶端可以呼叫來建立物件實例，並取得其指標。 所有這些函式都是以函式 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)為基礎，此函式會建立類別物件並提供指向介面的指標，該介面可讓您建立該類別的實例。 雖然必須有指出伺服器所在之系統的資訊，但用戶端不需要包含該資訊。 用戶端只需要知道 CLSID，絕對不能是伺服器程式碼的絕對路徑。 如需詳細資訊，請參閱 [透過類別物件建立物件](creating-an-object-through-a-class-object.md)。

## <a name="returning-a-pointer-to-a-separate-object"></a>將指標傳回給個別的物件

許多會將指標傳回給個別物件的介面方法，是建立並傳回 *列舉值物件* 之指標的許多介面方法，可讓您判斷物件所維護的指定類型有多少專案。 COM 會定義介面，以列舉各種不同的專案，例如字串、重要結構、名字和 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面指標。 建立列舉值實例並取得其介面指標的一般方式，就是從另一個介面呼叫方法。 例如， [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 介面會定義兩個方法（ [**EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise) 和 [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)），以傳回兩個不同列舉物件上介面的指標。 方法的 COM 中有許多其他範例會傳回物件的指標，例如 OLE 複合檔案介面 [**IOleObject：： GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)，在內嵌或連結的物件上呼叫時，會傳回容器物件的 [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)執行指標。

## <a name="implementing-an-object-through-which-to-pass-an-interface-pointer-directly-to-the-client"></a>執行將介面指標直接傳遞至用戶端的物件

當兩個物件（例如，OLE 複合檔案容器和伺服器）需要雙向通訊時，每個物件都會執行包含介面方法的物件，而介面方法可透過此方法將介面指標傳遞至另一個物件。 執行物件也是所建立物件的用戶端，接著可以呼叫方法，並取得傳遞的指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 用戶端和伺服器](com-clients-and-servers.md)
</dt> <dt>

[COM 伺服器責任](com-server-responsibilities.md)
</dt> </dl>

 

 





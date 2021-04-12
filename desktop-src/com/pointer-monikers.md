---
title: 指標標記
description: 指標標記會識別只能存在於作用中或正在執行狀態的物件。 這與其他標記類別不同，後者會識別可以存在於被動或主動狀態的物件。
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "104374194"
---
# <a name="pointer-monikers"></a>指標標記

*指標標記* 會識別只能存在於作用中或正在執行狀態的物件。 這與其他標記類別不同，後者會識別可以存在於被動或主動狀態的物件。

例如，假設應用程式有一個沒有持續表示的物件。 一般來說，如果您的應用程式用戶端需要存取該物件，您就可以直接將物件的指標傳遞給用戶端。 不過，假設您的用戶端預期會有一個名字標記。 無法使用檔案的標記來識別物件，因為它不會儲存在檔案中，也不會儲存在專案的標記中，因為它不包含在另一個物件中。

相反地，您的應用程式可以建立指標標記，也就是只在內部包含指標的標記，並將其傳遞至用戶端。 用戶端可以將此標記視為任何其他物件。 不過，當用戶端在指標名字標記上呼叫 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 時，標記代碼不會檢查執行中的物件資料表 (的 ROT) 或從儲存體載入任何內容。 相反地，標記程式碼只會在儲存于標記內的指標上呼叫 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 。

指標標記可讓只存在於作用中或執行中狀態的物件參與標記作業，並由標記用戶端使用。 指標名字和其他標記類別之間有一個重要的差異，就是無法將指標標記儲存至持續性儲存區。 如果您這樣做，呼叫 [**IMoniker：： Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) 方法會傳回錯誤。 這表示指標標記只有在特殊的情況下才有用。 如果您需要使用指標標記，可以使用 [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[反標記](anti-monikers.md)
</dt> <dt>

[類別名字標記](class-monikers.md)
</dt> <dt>

[複合的名字](composite-monikers.md)
</dt> <dt>

[檔案名字](file-monikers.md)
</dt> <dt>

[專案的名字](item-monikers.md)
</dt> </dl>

 

 





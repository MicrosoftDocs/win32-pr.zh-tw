---
title: OLE 元件物件模型
description: OLE 元件物件模型
ms.assetid: f3200d81-c2fa-4cc7-bf85-54f6c753a529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211c41de8c16eb1cabb1e62f475adbbf603e2c92
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "103933710"
---
# <a name="the-ole-component-object-model"></a>OLE 元件物件模型

AVIFile 程式庫所使用的物件都是 OLE 元件物件模型的一部分。 這主要是指它們共用一些可讓您更容易使用的方法，而它們所傳回的值是大部分 OLE 介面方法的通用值。

檔案和資料流程處理常式的 OLE 元件物件模型會使用 OLE **IClassFactory** 介面來建立其物件類別的實例。 作為元件物件時，它們會執行 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面，其中包含 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void))、 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)和 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 方法。 **IUnknown** 介面可讓應用程式取得相同物件所支援之其他介面的指標。

您可以使用 **QueryInterface** 方法來判斷物件是否支援特定介面。 如果物件支援指定的介面， **QueryInterface** 會傳回該介面的指標。

您可以使用 [**AddRef**](/previous-versions//dd757100(v=vs.85)) 和 [**發行**](/previous-versions//dd757102(v=vs.85)) 方法，來遞增和遞減與物件相關聯的參考計數。 參考計數可讓多個用戶端存取物件。 當第一個應用程式使用物件時，它的參考計數會設定為1。 然後，應用程式會使用 **AddRef** 方法來遞增計數，讓物件能夠追蹤其存取次數。

當應用程式使用物件完成時，它會呼叫 **Release** 方法來遞減參考計數。 當參考計數為零時，就不再需要物件， **釋放** 會釋出其使用的任何資源，並終結物件。 因為物件使用對應用程式而言是透明的內部資源，所以物件會負責釋放這些資源。 例如，在發行時，檔案處理常式可能需要關閉開啟的磁片檔案和可用的緩衝區記憶體。

大部分的 OLE 介面方法都會傳回使用 **HRESULT** 資料類型定義的結果控制碼。 此資料類型是由嚴重性代碼、內容資訊、設施碼和狀態碼所組成。 傳回結果控制碼，指出 success 的值為零。 非零值表示失敗，而傳回結果控制碼的狀態碼成員會提供其他轉譯的基礎。 如需 OLE 傳回結果控制碼的詳細資訊，請參閱 Ole 程式設計 *人員參考*。

 

 
---
title: 視覺標記法
description: 控制項支援在其容器中透過複合檔案技術以及牽涉到控制項及其容器的 OLE 拖放技術來定位並顯示本身。
ms.assetid: a7940560-360c-4c0d-9ac1-d051adb0b83e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9711dccbc7aa17f0b4a2ff228b2e2e4421e5083b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675812"
---
# <a name="visual-representation"></a>視覺標記法

控制項支援在其容器中透過複合檔案技術以及牽涉到控制項及其容器的 OLE 拖放技術來定位並顯示本身。 控制項必須能夠自行繪製，而容器則會管理控制項和其大小的位置。

控制項會加入至 OLE 檔所提供的基本函數。 控制項會呼叫其用戶端的 [**IOleClientSite：： RequestNewObjectLayout**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-requestnewobjectlayout) 方法，告知其容器想要變更其大小。 用戶端會呼叫控制項的 [**IOleObject：： GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent) 來取得新的大小，然後呼叫 [**IOleInPlaceObject：： SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects) 將控制項設定為新的大小。

僅支援 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) 或 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) 的控制項不支援透過 [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2) 進行快取，因為快取需要 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)的支援。 不過，這些控制項應提供方法讓用戶端透過 [**IDataObject：：**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) 轉譯控制項，讓用戶端可以選擇性地建立及管理自己的控制項呈現資料快取。

控制項使用 HIMETRIC 類型作為其座標。 不過，不同的容器可以使用不同的座標系統。 容器想要在自己的系統中接收座標，但控制項不一定知道其容器所使用的座標。 若要成功通訊，控制項需要將值轉換為其容器座標的方法。 容器會提供具有 [**>iolecontrolsite：： TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) 方法的網站物件。 控制項會先在容器的用戶端網站上呼叫這個方法，以將其座標轉換成容器的適當座標。 然後，它可以將轉換的座標傳遞給容器。

控制項可以在容器的網站物件中呼叫 [**>iolecontrolsite：： LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive) ，以防止容器嘗試將控制項從就地作用中狀態降級。 以這種方式降級控制項，會使控制項停用並終結視窗，因此如果控制項必須在已知的持續時間內維護其視窗，則可以呼叫 **LockInPlaceActive** 來保證其狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ActiveX 控制項](activex-controls.md)
</dt> </dl>

 

 





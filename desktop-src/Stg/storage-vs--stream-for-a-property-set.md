---
title: 屬性集的儲存體和資料流程物件
description: 程式設計人員指定在建立屬性集時，屬性集是否儲存在儲存體或資料流程中。
ms.assetid: d0ca649a-d405-4c34-af02-9c2ca8b2790e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e63ff148a72342da4cf5a6d8e1d59feab5c9b5b6fcbdf8a413069413cdb1e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661838"
---
# <a name="storage-and-stream-objects-for-a-property-set"></a>屬性集的儲存體和資料流程物件

程式設計人員指定在建立屬性集時，屬性集是否儲存在儲存體或資料流程中。 PROPSETFLAG \_ 簡單列舉值（以 *grfFlags* 參數傳遞給 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 方法）指出這一點。 設定屬性集儲存位置會提供適當的應用程式控制，以透過 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面與 COM 屬性集完全互通。

如果設定了 PROPSETFLAG \_ 簡單旗標，則會將屬性集儲存在儲存物件中，並將簡單屬性值寫入其中。 簡單值包括具有 VT  \_ 儲存體、VT \_ 資料流程、VT \_ 儲存 \_ 物件或 VT \_ 資料流程 \_ 物件之 VARTYPE 的值。 如需 **VARTYPE** 值和其使用方式的詳細資訊，請參閱 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構。

如果 \_ 未設定 PROPSETFLAG 簡單旗標，則只可將簡單的值寫入屬性集。

在簡單屬性集的儲存物件中，會建立名為「內容」的資料流程。 這是屬性集的主要資料流程，並保留所有簡單的屬性值。 簡單屬性值 (資料流程和儲存) 會儲存在屬性設定為子串流和儲存體的主要儲存物件下。 也就是說，這些簡單值會儲存為內容資料流程的同級。 同輩資料流程和儲存的名稱是由實作為來決定，並儲存在內容資料流程中，類似于儲存簡單字串屬性的方式。

 

 
---
description: 您可以使用介面儲存任何種類的應用程式特定資料。 例如，代表遊戲中地圖的表面可能包含地形的相關資訊。
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: '私用介面資料 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c010e24f691dc64c75e4dcea428af21d46ebfcb95b31775b9c8db81b2263e6d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520190"
---
# <a name="private-surface-data-direct3d-9"></a>私用介面資料 (Direct3D 9) 

您可以使用介面儲存任何種類的應用程式特定資料。 例如，代表遊戲中地圖的表面可能包含地形的相關資訊。

一個介面可以有一個以上的私用資料緩衝區。 每個緩衝區都是由您在將資料附加至介面時所提供的 GUID 所識別。

若要儲存私用表面資料，請使用 SetPrivateData，將指標傳遞至來源緩衝區、資料的大小，以及應用程式定義的資料 GUID。 （選擇性）來源資料可以以 COM 物件的形式存在;在此情況下，您會將指標傳遞至物件的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標，並設定 D3DSPD \_ IUNKNOWNPOINTER 旗標。

SetPrivateData 會配置資料的內部緩衝區，並將其複製。 然後您可以安全地釋放來源緩衝區或物件。 呼叫 FreePrivateData 時，會釋放內部緩衝區或介面參考。 這會在介面釋放時自動發生。

若要取得介面的私用資料，您必須配置正確大小的緩衝區，然後呼叫 GetPrivateData 方法，傳遞已指派給資料的 GUID。 您必須負責釋放您用於此緩衝區的任何動態記憶體。 如果資料是 COM 物件，這個方法會捕獲 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標。

如果您不知道要配置的緩衝區有多大，請先在 pSizeOfData 中呼叫 GetPrivateData （零）。 如果方法因 D3DERR MOREDATA 而失敗 \_ ，則會傳回緩衝區所需的位元組數目。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 表面](direct3d-surfaces.md)
</dt> </dl>

 

 

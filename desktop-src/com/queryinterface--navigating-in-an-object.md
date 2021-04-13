---
title: 在物件中流覽的 QueryInterface
description: 在物件中流覽的 QueryInterface
ms.assetid: 7dec015f-7609-40eb-a71e-f6e9c9b9f8ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dbd44d200bf0a992f47bc375d0782bdadacf6a3
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "104314078"
---
# <a name="queryinterface-navigating-in-an-object"></a>QueryInterface：在物件中流覽

當您在物件上取得介面的初始指標之後，COM 會有一個非常簡單的機制，可找出物件是否支援另一個特定介面，如果是，則會取得指標。  (如需取得物件介面之初始指標的詳細資訊，請參閱 [取得物件的指標](getting-a-pointer-to-an-object.md)。 ) 此機制是 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)介面的 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))方法。 如果物件支援要求的介面，則方法必須將指標傳回至該介面。 這可讓物件自由流覽物件所支援的介面。 **QueryInterface** 會將要求與「您是否支援指定的合約？」分隔 一旦協商成功，就能從該合約的高效能使用。

當用戶端一開始取得物件的存取權時，該用戶端最少會收到一個 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面指標 (最基本的介面) 透過此介面來控制物件的存留期，方法是在物件使用物件完成時告知物件，並叫用 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))。 用戶端會以程式設計的方式，要求它所管理的每個物件執行某些作業，但 **IUnknown** 介面沒有適用于這些作業的功能。 相反地，這些作業是透過其他介面來表示。 因此，用戶端會以程式設計方式與這些介面的物件進行協調。 具體而言，用戶端會呼叫 **QueryInterface** ，要求物件提供介面，用戶端可以透過此介面叫用所需的作業。

因為物件會執行 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))，所以它能夠接受或拒絕要求。 如果物件接受用戶端的要求， **QueryInterface** 會將所要求介面的新指標傳回給用戶端。 透過該介面指標，用戶端可以存取該介面的方法。 另一方面，如果物件拒絕用戶端的要求， **QueryInterface** 會傳回 null 指標（錯誤），而且用戶端沒有任何指標可呼叫所需的函數。 在此情況下，用戶端必須正常地處理這種可能性。 例如，假設用戶端在物件上有介面 A 的指標，並要求介面 B 和 C。假設物件也支援介面 B，但不支援介面 C。結果是物件會傳回 B 的指標，並回報不支援 C。

重點是，當物件拒絕對 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))的呼叫時，用戶端無法要求物件執行透過要求的介面表示的作業。 用戶端必須有介面指標，才能在該介面中叫用方法。 如果物件拒絕提供要求的指標，用戶端就必須做好準備而不需要執行任何動作，因為它不會執行任何動作來處理該物件，或是嘗試在另一個可能較不強大的介面上切換回來。 COM 功能的這項功能與其他物件導向的系統相較之下，您無法知道函式是否可以運作，直到您呼叫該函式，甚至是不確定處理失敗。 **QueryInterface** 提供可靠且一致的方式，以知道物件是否支援介面，然後再嘗試呼叫其方法。

[**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))方法也提供健全且可靠的方式，讓物件表示它不支援指定的合約。 亦即，如果在 **QueryInterface** 呼叫中，會詢問「舊」物件是否支援「新的」介面 (一種，例如，在舊物件已出貨) 之後，舊的物件就會可靠地，而不會造成損毀，請回答「否」。 支援此功能的技術是配置 Iid 所使用的演算法。 雖然這看起來很小一點，但對系統的整體架構而言非常重要，而且能夠查詢舊版專案的新功能，也就是在其他大部分的物件架構中不會有的功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用和執行 IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 





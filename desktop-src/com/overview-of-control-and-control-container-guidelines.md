---
title: 控制和控制容器指導方針
description: 控制和控制容器指導方針
ms.assetid: c4cf2409-0085-43e6-afa2-f9c03cc50565
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd72851775898f4fd140c7d101d72993c34e3eb
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "103679567"
---
# <a name="overview-of-control-and-control-container-guidelines"></a>控制和控制容器指導方針

ActiveX 控制項基本上是簡單的 OLE 物件，可支援 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面。 它通常會支援更多介面以提供功能，但所有其他介面可能會被視為選擇性，因此控制項容器不應依賴任何其他支援的介面。 藉由不指定控制項必須支援的其他介面，控制項可以有效率地鎖定特定功能區域，而不需要支援特定的介面來作為控制項。 如同使用 OLE，無論是在控制項或控制項容器中，絕對不應該假設介面可供使用，而且應該一律遵循標準的傳回檢查慣例。 如果無法使用所需的介面，控制項或控制容器必須正常地降級，並提供替代功能。

ActiveX 控制項容器必須能夠裝載基本的 ActiveX 控制項;它也會支援 [容器](containers.md)中指定的一些額外介面。 容器可以選擇性地支援許多介面和方法，這些介面和方法會分組為稱為 *元件類別* 的功能區域。 容器可支援元件類別的任何組合，例如，資料系結的元件類別存在，而且容器可能會支援資料系結功能，視容器的市場需求而定。 如果控制項需要容器的資料系結支援來運作，則會在登錄中輸入此需求。 如此一來，控制項容器就只能插入其知道可以成功裝載的控制項。 請務必注意，元件類別會指定為 OLE 的一部分，而且並非 ActiveX 控制項專用，而控制項架構會使用元件類別來識別 OLE 元件可能支援的功能區域。 元件類別並非累積或排除，因此控制項容器可以支援一個類別，而不一定支援另一個類別。

對於需要選擇性功能的控制項而言很重要，或特定容器的特定功能必須清楚地封裝並隨這些需求行銷。 同樣地，提供特定功能或元件類別的容器，必須在裝載 ActiveX 控制項時，以提供這些支援層級的方式進行行銷和封裝。 如果無法使用介面或方法，建議控制項盡可能以最多的容器做為目標和測試，並可正常地降級以提供較少或替代的功能。 如果控制項無法在不支援元件類別的情況下執行其指定的工作函式，則應該在登錄中輸入該類別做為需求，以防止控制項插入不適當的容器中。

這些指導方針會定義控制項可能會預期控制項容器可支援的介面和方法，不過當您在使用 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 或其他方法來取得這些介面的指標時，一定會有控制項檢查傳回值。 容器不應預期控制項支援超過 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面的任何內容，而且這些指導方針會識別控制項可支援的介面，以及特定介面的存在意義。

## <a name="why-the-activex-control-and-control-container-guidelines-are-important"></a>ActiveX 控制項和控制項容器指導方針的重要性

ActiveX 控制項已成為開發可程式化軟體元件的主要架構，可用於各種不同的容器，範圍從軟體發展工具到使用者生產力工具。 為了讓控制項可在各種不同的容器中運作正常，控制項必須能夠假設它可在所有容器中使用的最低層級功能。

藉由遵循這些指導方針，控制項和容器開發人員可讓其控制項和容器更可靠且互通，最後是更好且更有用的元件來建立以元件為基礎的解決方案。

## <a name="what-to-do-when-an-interface-you-need-is-not-available"></a>當您需要的介面無法使用時該怎麼辦

OLE 程式應該使用 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得介面指標，而且必須檢查傳回值。 OLE 應用程式無法安全地假設 **QueryInterface** 會成功。

這項需求適用于所有的 OLE 應用程式。 如果要求的介面無法使用 (也就是說， [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 會傳回 E \_ NOINTERFACE) ，則控制項或容器必須正常地降級，即使這表示它無法執行其指定的工作函式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ActiveX 控制項和控制項容器指導方針](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 





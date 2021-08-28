---
title: 內容容器
description: 內容容器
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Windows Media Player 線上商店、內容容器
- 線上商店、內容容器
- 輸入1個線上商店、內容容器
- Windows Media Player 線上商店、IWMPContentContainer 介面
- 線上商店、IWMPContentContainer 介面
- 輸入1個線上商店、IWMPContentContainer 介面
- Windows Media Player 內容容器
- Windows Media Player，IWMPContentContainer 介面
- 內容容器
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c582a04bd37e54a40f952402343c09fb7243fc07377ef7f507cc76f11390357c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123678"
---
# <a name="content-containers"></a>內容容器

Windows Media Player 使用內容容器來代表訂用帳戶下載或購買交易中的數位媒體內容。 內容容器會以 **IWMPContentContainer** 介面表示。 內容容器可能包含相關內容的清單，例如專輯或一組不相關的內容專案或 *追蹤*。 您可以使用 **IWMPContentContainer** 介面來列舉內容容器的追蹤，以及取得每個曲目的價格。您也可以取出內容容器本身的相關資訊，例如容器識別碼、容器中的內容類型，以及容器中的曲目總價格 (這可能與個別曲目的價格總和不同，就像是專輯購買) 一樣。

為了提供將多個內容容器封裝成單一物件的機制，Windows Media Player 支援 **IWMPContentContainerList** 介面。 **IWMPContentContainerList** 提供列舉和取出清單中內容容器的方法。 若要探索內容容器清單是否代表購買或訂閱下載，請呼叫 [IWMPContentContainerList：： GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) 來取得 [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) 值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於類型1線上商店**](about-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentContainer 介面**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[**IWMPContentContainerList 介面**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 





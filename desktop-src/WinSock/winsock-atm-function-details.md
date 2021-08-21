---
description: 根據針對 Windows 通訊端2與通訊協定無關的 multipoint/多播配置所定義的分類，ATM 會落在根資料和根控制項平面的類別中。
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Winsock ATM 函數詳細資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b089d02653ee996acc249f63144654c952ba724425fb208d9eb35cc9c2589e4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051376"
---
# <a name="winsock-atm-function-details"></a>Winsock ATM 函數詳細資料

根據針對 Windows 通訊端2與通訊協定無關的 multipoint/多播配置所定義的分類，ATM 會落在根資料和根控制項平面的類別中。  (參閱 Windows 通訊端 2 API 規格，附錄 D 以取得詳細資訊。 ) 作為根的應用程式會建立 c \_ 根通訊端，而分葉節點上執行的對應項會使用 c 分 \_ 葉通訊端。 根應用程式會使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 來加入新的分葉節點。 分葉節點上的對應應用程式，會將它們的 c \_ 分葉通訊端設定為接聽模式。 指定了 c \_ 根通訊端的 WSAJoinLeaf，將會對應至第一個分葉) 的安裝訊息 (，或針對任何後續的離開) 新增合作物件訊息 (。

> [!Note]  
> 針對任何後續的保留，在 **WSAJoinLeaf** 中指定的 QoS 參數，應該根據 ATM 論壇單向規格加以忽略。

 

分葉起始的聯結不是 ATM 單向3.1 的一部分，但在 ATM 單向4.0 中是支援的。 因此[](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) ，使用指定的 c 分 \_ 葉通訊端 WSAJoinLeaf 可以對應到適當的 ATM 單向4.0 訊息。

在 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)中指定的 condition 函式呼叫時，會在 *lpSQOS* 參數中修改對應的 LLI，以支援 AAL 參數和 B 協商。

> [!Note]  
> 只有這兩個中的特定欄位可以修改。 如需詳細資料，請參閱 ATM 論壇單向規格附錄 C 和附錄 F。

 

 

 




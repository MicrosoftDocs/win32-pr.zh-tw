---
title: 資料表示
description: 電腦架構可能會有明顯不同的運算環境。
ms.assetid: 34ba76ae-644d-4168-886f-0909a65f1abd
keywords:
- 遠端程序呼叫 RPC、描述、資料表示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9a0af96249c356f171396eaf52f91c5e33005eda080929cfbd8eecde27ffa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022088"
---
# <a name="data-representation"></a>資料表示

電腦架構可能會有明顯不同的運算環境。 為了配合這些差異，MIDL 可讓您修改表示資料的方式。 您有時可以將資料轉換成您的應用程式可以更輕鬆處理的格式，以簡化開發工作。 您可以改變應用程式的資料格式，讓它可以更有效率地透過網路傳輸。

**\[**[**傳送 \_ as**](/windows/desktop/Midl/transmit-as) **\]** 和 **\[** [**表示 \_ 為**](/windows/desktop/Midl/represent-as) **\]** 屬性，會指示編譯器將存根在用戶端和伺服器之間傳遞的 transmissible 型別與用戶端和伺服器應用程式使用的使用者類型產生關聯。 您必須提供在使用者類型和 transmissible 型別之間進行轉換的常式，以及釋放用來保存已轉換資料之記憶體的常式。 使用 [ **\[ 傳輸 \_ 為 \]** IDL] 屬性或 [ **\[ 表示 \_ 為 \]** ACF] 屬性，會指示存根在傳輸之前和之後呼叫這些轉換常式。 [ **\[** [**傳輸 \_ 為**](/windows/desktop/Midl/transmit-as)] **\]** 屬性可讓您將一種資料類型轉換成另一種資料類型，以便透過網路傳輸。 **\[**[**代表 \_ as**](/windows/desktop/Midl/represent-as) **\]** 屬性可讓您控制從網路到應用程式的資料呈現方式。

「 **\[** [**網路 \_ 封送**](/windows/desktop/Midl/wire-marshal)處理」 **\]** 和「 **\[** [**使用者 \_ 封送**](/windows/desktop/Midl/user-marshal)處理」 **\]** 屬性是憑證-DCE IDL 的 Microsoft 擴充功能。 其語法和功能類似于 DCE 指定的 **\[ 傳輸 \_ 方式 \]** ，而且會分別 **\[ 表示 \_ 為 \]** 屬性。 差別在於，您可以直接封送處理資料，而不是將資料從一種類型轉換成另一種類型。 若要這樣做，您必須提供外部常式來調整用戶端和伺服器端上的資料緩衝區大小、在用戶端和伺服器端上封送處理和封送處理資料，以及釋放伺服器端的資料。 MIDL 編譯器會產生格式代碼，以指示 NDR 引擎在需要時呼叫這些外部常式。

「 **\[ 網路 \_ 封 \] 送** 處理」和「 **\[ 使用者 \_ 封送 \]** 處理」屬性可讓您封送處理資料類型，否則無法跨進程界限傳輸這些資料類型。 此外，因為與類型轉換相關聯的額外負荷較少，所以在執行時間相較于 **\[ 傳送 \_ \] as** 和 **\[ 表示 \_ 為 \]**，連接 **\[ \_ 封送 \]** 處理和 **\[ 使用者 \_ 封送 \]** 處理可提供改善的效能。 「 **\[ 有線 \_ 封 \] 送** 處理」和「 **\[ 使用者 \_ 封送 \]** 處理」屬性彼此互斥，而且相對於「 **\[ 傳輸 \_ 為 \]** 」和「 **\[ 表示 \_ 為 \]** 指定類型的屬性」。

請務必注意，連接 **\[ \_ 封送 \]** 處理和 **\[ 使用者 \_ 封送 \]** 處理屬性的執行必須遵循憑證-DCE 規格所規定的封送處理規則。 基於這個理由，如果您不熟悉網路通訊協定，則不建議使用這些屬性。 有關 NDR 語法傳送的詳細資訊，可以在 [www.opengroup.org](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm)中找到。

本節將簡短介紹 MIDL 屬性的下列主題：

-   [**傳送 \_ as 和表示 \_ 為屬性**](the-transmit-as-and-represent-as-attributes.md)
-   [**網路 \_ 封送處理和使用者 \_ 封送處理屬性**](the-wire-marshal-and-user-marshal-attributes.md)

 

 
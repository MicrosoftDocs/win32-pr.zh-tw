---
title: 陣列和指標
description: 遠端程序呼叫 (RPC) 是設計來對開發人員而言是透明的。
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- 遠端程序呼叫 RPC、描述、陣列和指標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cc588d4db7cb222ec0fb2689bf645a2a7ed0e12b632392264d480c26777531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073498"
---
# <a name="arrays-and-pointers"></a>陣列和指標

遠端程序呼叫 (RPC) 是設計來對開發人員而言是透明的。 為了達成這個透明度，用戶端存根會將指標和指向的資料物件傳送至伺服器。 如果遠端程式變更資料，伺服器必須將新的資料傳送回用戶端，讓用戶端可以透過原始資料複製新的資料。

一般情況下，遠端程序呼叫的行為就像是本機程序呼叫一樣。 也就是說，當指標是參數時，遠端程式可以存取指標所參考的資料物件，就像本機程式一樣。

由於用戶端和伺服器程式是在不同的位址空間中執行，因此開發人員必須使用 Microsoft 介面定義語言 (MIDL) 屬性來描述在用戶端與伺服器之間傳輸陣列和指標資料的方式。 本節將概述如何在分散式應用程式中使用陣列和指標，請參考下列主題：

-   [陣列和 RPC](arrays-and-rpc.md)
-   [指標和 RPC](pointers-and-rpc.md)
-   [使用陣列、字串和指標](using-arrays-strings-and-pointers.md)

 

 





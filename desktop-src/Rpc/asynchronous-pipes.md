---
title: 非同步管道
description: 使用具有非同步 RPC 的管道參數，可讓您以累加方式傳送資料，因為它可供使用，而不會佔用用戶端和伺服器。
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0957b1ddc381d2a91b77033842b2807ed8a9dd34718d0148d6853083229d408d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023788"
---
# <a name="asynchronous-pipes"></a>非同步管道

使用具有非同步 RPC 的 [管道](/windows/desktop/Midl/pipe) 參數，可讓您以累加方式傳送資料，因為它可供使用，而不會佔用用戶端和伺服器。 當您有大量的資料要傳輸、與緩慢的用戶端、緩慢的伺服器或慢速網路合併時，這項功能特別有用。 如果您在非同步函式呼叫中使用管道，則會以非同步管道的定義來進行。 同步管道不支援與非同步函式一起使用。

不同于傳統 (同步) 管道，伺服器會在其中處理傳送和接收管道資料的所有詳細資料，非同步管道是對稱的。 亦即，用戶端和伺服器都可以透過管道推送和提取資料。

> [!Note]  
> 只能以傳址方式傳遞管道參數。 即使 IDL 檔案顯示以傳值方式傳遞的 [管道](/windows/desktop/Midl/pipe) 參數，產生的存根還是只會以傳址方式接受管道參數。

 

在下列非同步管道的討論中，會假設您熟悉管道類型的函式。 如需有關這些主題所述之管道程式的詳細資訊，請參閱 [管道](pipes.md)。

 

 
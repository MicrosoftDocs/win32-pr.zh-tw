---
description: 找出要啟用的元件
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: 找出要啟用的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104571572"
---
# <a name="locating-a-component-for-activation"></a>找出要啟用的元件

當 COM + 找到正確的資料分割時（透過使用者識別的預設資料分割集、資料分割的名字，或物件內容中的資料分割識別碼），COM + 必須在該資料分割內找出正確的元件。 下圖顯示元件位於分割區時，如何找到和啟動元件。

> [!Note]  
> 在啟動任何元件之前，COM + 會執行驗證，以確認嘗試啟用元件的使用者身分識別是否有許可權可以存取元件所在的分割集。

 

![此圖顯示用於尋找要啟用之元件的疑難排解樹狀目錄。](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

上圖顯示下列內容：

-   如果所呼叫的元件位於分割區中，而且與呼叫元件位於相同的應用程式中，則不論所呼叫的元件是否標記為公用或私用，元件都會啟用。
-   如果所呼叫的元件位於分割區中，但不存在於與呼叫元件相同的應用程式中，COM + 會檢查元件是否標記為公用。 如果找不到任何公用版本，COM + 會搜尋全域分割區，以找出元件的公用版本。 如果在全域分割區中找不到元件的公用版本，或如果使用者身分識別沒有分割區的許可權，則啟用會失敗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在啟用期間尋找磁碟分割](locating-partitions-during-activation.md)
</dt> </dl>

 

 




---
description: 提供一些緩衝區溢位情況的簡介，並提供一些構想和資源，協助您避免建立新的風險並減輕現有的風險。
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: 避免緩衝區溢位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990354"
---
# <a name="avoiding-buffer-overruns"></a>避免緩衝區溢位

緩衝區溢位是最常見的安全性風險來源之一。 緩衝區溢位的原因基本上是將未選取的外部輸入視為值得信任的資料。 使用 [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85))、 **strcat**、 **strcpy** 或 **wcscpy** 等作業來複製此資料的動作，可能會產生非預期的結果，以允許系統損毀。 在最佳情況下，您的應用程式將會中止，併發生核心傾印、分割錯誤或存取違規。 在最糟的情況下，攻擊者可以在您的程式中引進和執行其他惡意程式碼，以利用緩衝區溢位。 將未選取的輸入資料複製到以堆疊為基礎的緩衝區是可被利用的錯誤最常見的原因。

緩衝區溢位可能會以各種不同的方式發生。 下列清單提供一些緩衝區溢位情況的簡介，並提供一些構想和資源，協助您避免建立新的風險並減輕現有的風險：

<dl> <dt>

<span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>靜態緩衝區溢出
</dt> <dd>

當已在堆疊上宣告的緩衝區寫入的資料量超過配置用來保存的緩衝區時，就會發生靜態緩衝區溢出。 當未驗證的使用者輸入資料直接複製到靜態變數時，會發生此錯誤的較不明顯版本，進而造成潛在的堆疊損毀。

</dd> <dt>

<span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>堆積溢出
</dt> <dd>

堆積溢出（例如靜態緩衝區溢出）可能會導致記憶體和堆疊損毀。 由於堆積溢出發生在堆積記憶體中，而不是在堆疊上，有些人認為它們比較不能造成嚴重的問題;然而，堆積溢出需要真正的程式設計護理，而且能夠讓系統的風險成為靜態緩衝區溢出。

</dd> <dt>

<span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>陣列索引錯誤
</dt> <dd>

陣列索引錯誤也是記憶體溢出的來源。 謹慎的界限檢查和索引管理將有助於防止這種類型的記憶體溢出。

</dd> </dl>

避免緩衝區溢位主要是關於撰寫良好的程式碼。 請一律驗證所有輸入，並在必要時正常失敗。 如需撰寫安全程式碼的詳細資訊，請參閱下列資源：

-   Maguire、Steve \[ 1993 \] 、 *撰寫穩固* 的程式碼、ISBN 1-55615-551-4、Microsoft 按壓、Redmond、華盛頓州。
-   Howard、Michael 和 LeBlanc、David \[ 2003 \] 、 *撰寫安全* 的程式碼、2d ed、ISBN 0-7356-1722-8、Microsoft 按壓、Redmond、華盛頓州。

> [!Note]  
> 某些語言和國家/地區可能無法使用這些資源。

 

安全字串處理是一種長期的問題，可繼續透過下列良好的程式設計實務來解決這兩個問題，而且通常會使用安全的字串處理函式來修整現有的系統。 適用于 Windows shell 的這類一組函式範例會以 [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata)開始。

 

 

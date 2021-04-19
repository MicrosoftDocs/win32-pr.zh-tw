---
description: 應用程式必須為此資料配置記憶體;TAPI 和服務提供者會提供資料。 如果作業是非同步，則在非同步回復訊息表示成功之前，無法使用資料。
ms.assetid: 61313fe3-74a1-4195-b5af-37463dad02c1
title: 記憶體配置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f192e34fdc652293c480277631c3839ecd2435fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970129"
---
# <a name="memory-allocation"></a>記憶體配置

應用程式必須為此資料配置記憶體;TAPI 和服務提供者會提供資料。 如果作業是非同步，則在非同步回復訊息表示成功之前，無法使用資料。

用來在應用程式與 TAPI 之間傳遞資料的所有資料結構都會 *壓平* 合併。 也就是說，資料結構不包含子結構的指標，其中包含大小可變大小的資料元件。 相反地，用來將可變數據量傳回給應用程式的資料結構必須具有下列中繼架構：

``` syntax
  DWORD  dwTotalSize;
  DWORD  dwNeededSize;
  DWORD  dwUsedSize; 
    <fixed size fields> 
  DWORD  dw<VarSizeField1>Size;
  DWORD  dw<VarSizeField1>Offset; 
    <fixed size fields> 
  DWORD  dw<VarSizeField2>Size;
  DWORD  dw<VarSizeField2>Offset; 
    <common extensions> 
    <var sized field1> 
    <var sized field2>
```

**DwTotalSize** 成員是配置給此資料結構的大小（以位元組為單位）。 它會標示資料結構的結尾，並由應用程式設定，然後再叫用使用此資料結構的函數。 函式不會讀取或寫入超過此大小。 應用程式必須設定 **dwTotalSize** 成員，以表示配置給 TAPI 的總位元組數，以傳回結構的內容。

TAPI 會填入 **dwNeededSize** 成員。 它會指出需要多少位元組才能傳回所有要求的資料。 大小可變大小欄位的存在通常會讓應用程式無法估計配置所需的資料結構大小。 這個欄位會傳回資料實際所需的位元組數目。 這個數位可能小於、等於或大於 **dwTotalSize**，而且會包含 **dwTotalSize** 成員本身的空間。 如果較大，則只會部分填滿傳回的結構。 如果部分結構中有應用程式所需的欄位，就不需要執行任何其他動作。 否則，應用程式應至少配置 **dwNeededSize** 大小的結構，然後再次叫用函式。 通常，您可以使用足夠的空間來傳回所有資訊，雖然可能會再次增加大小。

如果 TAPI 將資料傳回給應用程式，則會填滿 **dwUsedSize** 成員，以表示包含有用資料之資料結構部分的實際大小（以位元組為單位）。 舉例來說，如果配置的結構太小，而截斷的欄位是大小可變大小的欄位，則 **dwNeededSize** 大於 **dwTotalSize**，且截斷的欄位會保留空白。 因此， **dwUsedSize** 成員可能小於 **dwTotalSize**。 部分域值不會傳回。

遵循此標頭是資料結構的固定部分。 它包含一般欄位和大小/位移組，以描述實際的大小可變大小欄位。 [位移] 欄位包含從記錄開頭大小可變大小欄位的位移（以位元組為單位）。 [大小] 欄位包含大小可變大小欄位的大小（以位元組為單位）。 如果 [大小可變大小] 欄位是空的，則 [大小] 欄位為零，而且位移設定為零。 大小可變已調整大小的欄位如果總結構大小不足，則會被截斷。 也就是說，其 size 欄位設定為零，而且位移設定為零。 大小可變大小的欄位會在固定欄位之後。

如果服務提供者必須填入變數成員，TAPI 會將對應的大小和位移成員初始化為零。 如果服務提供者填滿變數成員，它就必須將對應的大小和位移成員設定為適當的值，包括 **dwUsedSize** 和 **dwNeededSize** （如果設定變數成員的話）。 服務提供者不得截斷變數成員，使其符合可用的空間。

服務提供者必須在結構的固定成員之後立即啟動變數成員，並且在配置的記憶體結尾留下任何額外的空間，讓 TAPI 可將它用於可變長度的成員。 它可以依任何順序放置變數成員，但成員必須是連續的。

 

 




---
title: 範圍
description: 範圍
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- 文字服務架構 (TSF) 、範圍
- TSF (文字服務架構) ，範圍
- 文字服務，範圍
- 啟用 TSF 的應用程式，範圍
- 範圍
- 文字服務架構 (TSF) 、錨點
- TSF (文字服務架構) 、錨點
- 文字服務，錨點
- 啟用 TSF 的應用程式，錨點
- 錨點
- 文字服務架構 (TSF) ，複製
- TSF (文字服務架構) ，複製
- 文字服務，複製
- 啟用 TSF 的應用程式，複製
- 克隆
- 文字服務架構 (TSF) ，備份
- TSF (文字服務架構) ，備份
- 文字服務，備份
- 啟用 TSF 的應用程式，備份
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932554"
---
# <a name="ranges"></a>範圍

## <a name="anchors"></a>錨點

範圍是由兩個 *錨* 點（開始錨點和結束錨點）所分隔。 錨點存在於兩個字元之間的虛數中。 [開始] 錨點與錨點後面的文字相關，而端點錨點與錨點前面的文字相關。 開始和結束錨點都可以存在於相同的位置。 在此情況下，範圍的長度為零。

例如，以下列文字開頭：


```C++
This is text.
```



現在將範圍套用至具有起點和結尾錨點（位於位置0）的這個文字。 它會以視覺化方式呈現：


```C++
<anchor></anchor>This is text.
```



錨點不會佔用文字本身內的任何空間。 這是長度為零的範圍，其文字為空白。

現在將結束錨點 + 3 個位置移位。 它會以視覺化方式呈現：


```C++
<anchor>Thi</anchor>s is text.
```



開始錨點位於位置0的字元之前，而結束錨點則位於位置3的字元之後，因為結束錨點已移至右邊的3個位置。 文字範圍現在是 "Thi"。

此外，您無法在結束錨點之後進行啟動錨點，也無法在起始錨點前面建立端點錨點。

## <a name="anchor-gravity"></a>錨點引力

每個錨點都有一個 *重力* 設定，可決定當文字插入文字資料流程的錨點位置時，錨點的回應方式。 在錨點的位置進行插入時，必須在錨點的位置中進行調整。 重心會決定如何調整此錨點位置。

例如：


```C++
It is <anchor></anchor>cold today.
```



如果在範圍位置插入 "非常" 這個字，則開始錨點可以放置在插入的單字之前或之後：


```C++
It is <anchor>very </anchor>cold today.
```



\- 或 -


```C++
It is very <anchor></anchor>cold today.
```



錨點重力會指定在插入位置時，錨點重新置放的方式。 重心 *可以是回溯或**轉寄*。

如果錨點有回溯引力，則在插入時，錨點會向後移動（相對於插入點），使插入的文字在錨點之後：


```C++
It is <anchor>very </anchor>cold today.
```



如果錨點具有向前引力，則錨點會向前移動 (相對於插入點) 插入點，使插入的文字在錨點之前：


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a>複製和備份

有兩種方式可以建立範圍物件的「複製」。 第一個是使用 [ITfRange：： clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone)建立範圍的 *複本*。 第二個則是使用 [ITfCoNtext：： CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup)進行範圍 *備份*。

複製是不包含靜態資料之範圍的複本。 系統會複製範圍的錨點，但複製仍會涵蓋內容中的文字範圍。 複製是所有方面的範圍物件。 這表示複製範圍的文字和屬性是動態的，如果複製所涵蓋之範圍的文字及/或屬性變更，則會變更。

備份會在備份做為靜態資料時儲存範圍的文字和屬性。 備份也會複製原始範圍，以便追蹤原始範圍的大小和位置變更。 這表示備份範圍的文字和屬性是靜態的，而且如果備份所涵蓋之範圍的文字及/或屬性變更，則不會變更。

例如，下列範圍 (在內容中 pRange) ：


```C++
"This is some <pRange>text</pRange>."
```



現在，請複製此範圍並進行備份：


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



現在，物件包含下列各項：


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



現在變更 pRange 的文字：


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



現在，物件包含下列各項：


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



設定文字會導致內容中的文字變更。 它也會造成 pRange 和 pClone 的結束錨點變更。 pClone 現在包含「其他文字」，因為在範圍內變更文字，而這些變更會由所有範圍追蹤。 當 pRange 和 pClone 所涵蓋的文字變更時，pClone 的文字也會變更。

PBackup 中的文字未與原始 pRange 變更，因為備份中) 的 (資料與內容無關，而且會分開儲存。 備份中包含的複製實際上會變更，但資料是靜態的。

還原備份時，可以將備份套用到備份內的複製或完全不同的範圍。 若要將備份套用到備份內的複製，請將 **Null** 傳遞至 [ITfRangeBackup：： Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) ，如下列程式碼範例所示：


```C++
pBackup->Restore(ec, NULL);
```



現在，物件包含下列各項：


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



若要將備份還原至不同的範圍，請在呼叫 **ITfRangeBackup：： restore** 時傳遞範圍物件的指標。 備份的文字和屬性將會套用至新的範圍。 例如，在 **還原** 呼叫之前使用上述範例，將會修改 pRange 以示範這一點：


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



現在，物件包含下列各項：


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



當 pRange 的結束錨點移至左邊的兩個位置時，pClone 的結束錨點不會變更。

現在使用 pRange 還原備份，並使用下列程式碼範例：


```C++
pBackup->Restore(ec, pRange);
```



現在，物件包含下列各項：


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



PRange 所涵蓋的文字已取代為 "text"、pClone 所涵蓋的部分文字已變更，以及 pBackup 變更以符合 pRange。

 

 





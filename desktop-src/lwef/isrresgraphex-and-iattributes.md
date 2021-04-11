---
title: ISRResGraphEx 和 IAttributes
description: ISRResGraphEx 和 IAttributes
ms.assetid: 6eb37da1-5252-4c41-891c-c19cca6fb7d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659d7d4723bfc5145fb8abcc77043031a0e48e8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023304"
---
# <a name="isrresgraphex-and-iattributes"></a>ISRResGraphEx 和 IAttributes

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

引擎所傳回的結果物件必須支援 ISRResGraphEx 介面和 IAttributes 介面。 只支援 ISRResGraphEx 介面足以讓音效編輯器提供斷字資訊，但不會提供音素資訊的必要支援。

音效編輯器會要求引擎也支援特殊的 DWord 屬性 **SRATTR \_ PHONESEG**。 編輯器會查詢引擎以查看 IAttributes 介面，並嘗試將 **SRATTR \_ PHONESEG** 設定為1。 如果該呼叫成功，音效編輯器會假設引擎的結果會支援從結果物件收集音素分割資訊。

`#define    SRATTR_PHONESEG    MAKELONG (1, SRVEN_MICROSOFT)`

當結果物件傳送至音效編輯器時，它會查詢該物件以執行 ISRResGraphEx。 ISRResGraphEx 包含具有類型簽章的成員函式 DataGet

`HRESULT  DataGet  (DWord, dwID, GUID gAttrib, SDATA *psData)`

其中 **dwID** 是繪圖物件的識別碼， **gAttrib** 是對應至所搜尋屬性的 GUID，而 **psData** 是包含傳回之資料的 .sdata 物件指標。 引擎負責透過 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)配置儲存在 **psData** 中的資料。 在此情況下，呼叫應用程式 (在此情況下，音效編輯器) 負責在完成時透過 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 釋放。

需要 DataGet 才能辨識三個預先定義的 Guid，這些 Guid 列于 SAPI 檔中。 當使用對應至圖形中邊緣的 **PHONEMESEGMENTATION** 呼叫 DWORDSet 時，若引擎會傳回成功的程式碼給 **(SRATTR \_ PHONESEG，1)** 也需要辨識特定的 GUID **SRGARC \_ dwID**。

`DEFINE_GUID(SRGARC_PHONMESEGMENTATION, 0xd05405b0, 0x1db1, 0x11d2, 0x94, 0x2, 0x0, 0xc0, 0x4f, 0x8e, 0xf4, 0x8f);`

當呼叫傳回時， **psData** 應該指向 **PHONESEG** 類型之 DWORD 對齊結構的陣列，由定義：

``` syntax
typedef struct tagSRPHONESEG {
   DWORD   dwSize;       // Size of the SRPHONESEG structure + phone data
   QWORD   qwStartTime;  // SAPI timestamp of the start of the seqment
   …QWORD   qwEndTime;    // SAPI timestamp of the end of the seqment
   int      nScore;      // The segment's score
   WCHAR   aPhones[0];   // Array of phone(s) making up the segment
} SRPHONESEG,  *PSRPHONESEG;
```

其中 **qwStartTime** 和 **qwEndTime** 指向每個音素的開頭和結尾組成邊緣所涵蓋的單字，而 **aPhones** 是 Unicode 字元的陣列，對應至電話的 IPA 標記法，這會在此區段中產生。  (在某些語言中，有一個具有多個 IPA 音素的拼寫音素。 例如，在英文中，"live" 單字中的「長 I」音效其實是一種 diphthong，由兩個較簡單的音素串連在一起。 ) **aPhones** 陣列應以零終止，並在結尾填補，讓陣列中的每個 **SRPHONESEG** 結構長度都是四個位元組的倍數。

例如，假設在弧形4上說出的單字是「已建立」。 然後，對 DataGet (4、 **SRGARC \_ PHONEMESEGMENTATION**、&sd) 的呼叫可能會傳回三個音素區段的陣列、/m/ **從 qwStartTime**= 328434 個位元組執行至 **qwEndTime**= 330354 個位元組、 **/1e/從 qwStartTime = 330354** 個位元組執行至 **qwEndTime = 344114** 個位元組，以及/d/從 **qwStartTime**= 344114 位元組執行至 **qwEndTime**= 347314 位元組。 這些會以三個 **SRPHONESEG** 結構的封裝陣列形式呈現，分別為28、32和28個位元組大小。 請注意，中間 **SRPHONESEG** 結構的結尾有一些填補，因此陣列中的下一個專案會從4位元組界限開始。

SAPI 4.0 SDK 包含 (SRFunc) 的工具，可用於測試與 SAPI 4.0 規格的合規性。包含在該工具中的測試是與這組介面相容的測試。 這項工具的原始程式碼是不錯的起點，可讓您瞭解這些介面如何與音效編輯器互動，以及如何在開發期間進行介面的調試。

 

 
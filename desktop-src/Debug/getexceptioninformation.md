---
description: 抓取與電腦無關的例外狀況描述，以及發生例外狀況時，執行緒存在的電腦狀態相關資訊。 您只能從例外狀況處理常式的篩選運算式內呼叫這個函數。
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: GetExceptionInformation 宏
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689123"
---
# <a name="getexceptioninformation-macro"></a>GetExceptionInformation 宏

抓取與電腦無關的例外狀況描述，以及發生例外狀況時，執行緒存在的電腦狀態相關資訊。 您只能從例外狀況處理常式的篩選運算式內呼叫這個函數。

> [!Note]  
> Microsoft C/c + + 優化編譯器會將此函式解釋為關鍵字，而在適當的例外狀況處理語法外部使用會產生編譯器錯誤。

 

## <a name="syntax"></a>語法


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a>參數

這個宏沒有任何參數。

## <a name="return-value"></a>傳回值

[**例外狀況 \_ 指標**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)結構的指標，其中包含下列兩個結構的指標：

-   [**例外 \_ 狀況**](/windows/desktop/api/WinNT/ns-winnt-exception_record) 包含例外狀況描述的記錄結構。
-   包含電腦狀態資訊的 [**內容**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)結構。

## <a name="remarks"></a>備註

用來呼叫函式的篩選運算式 () 如果在 **\_ \_ try** 區塊執行期間發生例外狀況，則會進行評估，而且它會判斷 **\_ \_ except** 區塊是否執行。

篩選運算式可以叫用篩選函數。 篩選函數無法呼叫 **GetExceptionInformation**。 不過， **GetExceptionInformation** 的傳回值可以做為參數傳遞至篩選函數。

若要將 [**例外狀況 \_ 指標**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) 資訊傳遞給例外狀況處理常式區塊，篩選運算式或篩選函數必須將指標或資料複製到可供處理常式稍後存取的安全儲存區。

在嵌套處理常式的情況下，會評估每個篩選運算式，直到一個評估為 **例外狀況 \_ 執行 \_ 處理常式** 或 **例外狀況 \_ 繼續 \_ 執行** 為止。 每個篩選運算式都可以叫用 **GetExceptionInformation** 來取得例外狀況資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**上下文**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[**例外狀況 \_ 指標**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[**例外狀況 \_ 記錄**](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[**GetExceptionCode**](getexceptioncode.md)
</dt> <dt>

[**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[結構化例外狀況處理函式](structured-exception-handling-functions.md)
</dt> <dt>

[結構化例外狀況處理總覽](structured-exception-handling.md)
</dt> <dt>

[啟用 Intel AVX 的 Windows 支援](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 

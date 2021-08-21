---
description: 本主題中所述的許多偵錯工具都是在 DirectShow 基類庫中執行。 如需詳細資訊，請參閱 DirectShow 基類。
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: DirectShow 篩選的調試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54532b68df09b78b3b03aa95d7dda5c84cdf7d770cffd131e47228e6d88cba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953287"
---
# <a name="debugging-directshow-filters"></a>DirectShow 篩選的調試

本主題中所述的許多偵錯工具都是在 DirectShow 基類庫中執行。 如需詳細資訊，請參閱[DirectShow 基類](directshow-base-classes.md)。

## <a name="assertion-checking"></a>判斷提示檢查

使用判斷提示檢查壓縮。 判斷提示可以驗證您在程式碼中針對前置條件與後置條件進行的假設。 DirectShow 提供數個判斷提示宏。 如需詳細資訊，請參閱 [Assert 和中斷點宏](assert-and-breakpoint-macros.md)。

## <a name="object-names"></a>物件名稱

在 debug 組建中，有一個從 [**CBaseObject**](cbaseobject.md) 類別衍生的全域物件清單。 建立物件時，會將它們新增至清單。 當它們損毀時，就會從清單中移除它們。 若要顯示這些物件的清單，請呼叫 [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) 函數。

[**CBaseObject**](cbaseobject.md)基類的函式方法（和其衍生的大部分類別）包含物件名稱的參數。 提供物件的唯一名稱來識別它們。 當您宣告名稱時，請使用 [**name**](name.md) 宏，如此就只會在 debug 組建中配置此名稱。 在零售組建中，名稱會變成 **Null**。

## <a name="debug-logging"></a>偵錯記錄

當程式執行時， [**DbgLog**](dbglog.md) 函式會顯示偵錯工具的訊息。 您可以使用此函式來追蹤應用程式或篩選的執行。 您可以記錄傳回碼、變數值，以及任何其他相關資訊。

每個偵錯工具訊息都有一種類型，例如記錄 \_ 追蹤或記錄檔 \_ 錯誤，以及表示訊息重要性的調試層級。 具有較低 debug 層級的訊息比較高層級的訊息更重要。

在下列範例中，假設的篩選會將 pin 與 pin 陣列中斷連線。 如果中斷連接嘗試成功，則篩選會顯示記錄 \_ 追蹤訊息。 如果嘗試失敗，則會顯示記錄 \_ 錯誤訊息：


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



當您正在進行偵錯工具時，您可以設定每個訊息類型的 debug 層級。 此外，每個模組 (DLL 或可執行檔) 都會維護它自己的調試層級。 如果您要測試篩選，請針對包含篩選的 DLL，引發偵錯工具層級。

如需詳細資訊，請參閱 [Debug Output 函數](debug-output-functions.md)。

## <a name="critical-sections"></a>重要區段

為了讓您更容易追蹤鎖死，請包含判斷呼叫程式碼是否擁有指定的重要區段的判斷提示。 [**CritCheckIn**](critcheckin.md)和 [**CritCheckOut**](critcheckout.md)函數會指出呼叫執行緒是否擁有重要區段。 一般來說，您會從 assert 宏內部呼叫這些函式。

您也可以使用 [**DbgLockTrace**](dbglocktrace.md) 函式來追蹤何時保留或釋放重要區段。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的調試](debugging-in-directshow.md)
</dt> </dl>

 

 




---
description: WMI 查詢語言 (WQL) 是標準美國國家標準局結構化查詢語言 (SQL)  (ANSI SQL) 的子集，其中包含支援 WMI 的次要語義變更。
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: 使用 WQL 查詢
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 737ae9505a0f775c26c5049eeb2f8500c9e3222d78181e18326ff53d39dfde01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554829"
---
# <a name="querying-with-wql"></a>使用 WQL 查詢

WMI 查詢語言 (WQL) 是標準美國國家標準局結構化查詢語言 (SQL)  (ANSI SQL) 的子集，其中包含支援 WMI 的次要語義變更。

如需支援的 wql 關鍵字的完整清單，請參閱[WMI) 的 wql (SQL ](wql-sql-for-wmi.md)。 針對物件或屬性名稱使用 SQL 關鍵字可能會限制無法剖析查詢。 下列 SQL 關鍵字受到限制： **Null**、 **TRUE** 和 **FALSE**。

> [!Note]  
> WQL 查詢中可使用的和和或關鍵字數目有一些限制。 複雜查詢中使用的大量 WQL 關鍵字可能會導致 WMI 將 **WBEM \_ E \_ 配額 \_ 違規** 錯誤碼傳回為 **HRESULT** 值。 WQL 關鍵字的限制取決於查詢的複雜程度。

 

查詢可以使用 **WHERE** 子句進行擴充和自訂，但不是必要的。 **WHERE** 子句是由屬性或關鍵字、運算子和常數所組成。 所有 **WHERE** 子句都必須指定 WQL 中包含的其中一個預先定義的運算子。 如需語法的詳細資訊，請參閱 [WHERE 子句](where-clause.md)。 如需有效 WQL 運算子的詳細資訊，請參閱 [Wql 運算子](wql-operators.md)。

如同其他 SQL 查詢字串，您可以對查詢進行 escape。

> [!Note]  
> WQL 不支援跨命名空間的查詢或關聯。 您無法在目的電腦上的所有命名空間中查詢指定類別的所有實例。

 

WQL 支援下列類型的查詢：

-   資料查詢

    資料查詢是用來取出類別實例和資料關聯。 它們是 WMI 腳本和應用程式中最常使用的查詢類型。 如需資料查詢語法的詳細資訊，請參閱 [要求類別實例資料](requesting-class-instance-data.md)。 如需關聯的詳細資訊，請參閱宣告 [關聯類別](declaring-an-association-class.md)。

    > [!Note]  
    > WQL 不支援陣列資料類型的查詢。

     

    下列資料查詢範例會從所有 [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)實例要求名為 "Application" 的事件記錄檔。

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   事件查詢

    取用者會使用事件查詢來註冊，以接收事件的通知。 事件提供者會使用事件查詢來註冊，以支援一或多個事件。 如需事件查詢的詳細資訊，請參閱 [接收事件通知](receiving-event-notifications.md)。

    當衍生自 [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) 之類別的新實例建立時，暫存事件取用者會使用下列範例事件查詢來要求通知。

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   架構查詢

    架構查詢是用來取出類別定義 (而非) 和架構關聯的類別實例。 類別提供者會使用架構查詢來指定它們在註冊時所支援的類別。 如需架構查詢的詳細資訊，請參閱 [取出類別定義](retrieving-class-definitions.md)。

    下列範例架構查詢會顯示特殊語法。

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 日期和時間格式](date-and-time-format.md)
</dt> </dl>

 

 

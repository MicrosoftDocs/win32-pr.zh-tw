---
description: 傳統提供者應該使用受控物件格式 (MOF) 來發佈其事件資料的配置。 接著，取用者可以在執行時間從 WMI 讀取已發佈的配置，並用它來讀取事件資料。
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: 發佈傳統提供者的事件架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f51cfd30d0c9d73841ca906fb81e9d544dec88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318528"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a>發佈傳統提供者的事件架構

[傳統](about-event-tracing.md) 提供者應該使用 [受控物件格式](../wmisdk/managed-object-format--mof-.md) (MOF) 來發佈其事件資料的配置。 接著，取用者可以在執行時間從 WMI 讀取已發佈的配置，並用它來讀取事件資料。

如果您使用 MOF 來發佈 WMI 中的事件資料版面配置，通常會在根 WMI 命名空間中建立下列三種類型的 MOF 類別 \\ ：

-   [提供者 MOF 類別](#provider-mof-classes)
-   [一或多個事件 MOF 類別](#event-mof-classes)
-   [一或多個事件種類 MOF 類別](#event-type-mof-classes)

## <a name="provider-mof-classes"></a>提供者 MOF 類別

如果您發佈事件資料的配置，您必須建立識別提供者的 MOF 類別。 此類別必須衍生自 **EventTrace** MOF 類別，而且必須是空的 (沒有任何屬性或方法) 。 類別也必須包含可唯一識別提供者的 **Guid** 限定詞。 這與您在呼叫 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 函式來註冊提供者時所使用的 GUID 相同。

## <a name="event-mof-classes"></a>事件 MOF 類別

事件 MOF 類別會定義提供者所提供之事件的類別。 這個類別衍生自提供者 MOF 類別，而且必須是空的 (沒有任何屬性或方法) 。 類別也必須包含 **Guid** 辨識符號，以唯一識別其子類別所定義的事件類別。 在設定 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的 **guid** 成員時，提供者會使用這個相同的 guid。

## <a name="event-type-mof-classes"></a>事件種類 MOF 類別

事件種類 MOF 類別會定義實際的事件資料。 此類別衍生自其父事件 MOF 類別。 為事件種類 MOF 類別命名時，慣例是在事件種類 MOF 類別名稱的開頭使用事件 MOF 類別名稱。 例如，如果事件 MOF 類別名稱是 HWConfig，而事件種類 MOF 類別代表 CPU 資訊，您應該將事件種類的 MOF 類別命名為 HWConfig \_ cpu。

使用事件種類 MOF 類別上 **的 [事件** 類型] 限定詞來識別事件種類。 如果多個事件種類使用相同的事件資料，則可以使用相同的 MOF 類別。 在設定類別時，提供者會使用相同的事件種類值來識別事件。[**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的 **類型** 成員。

事件種類 MOF 類別包含屬性。 這些屬性的順序會定義事件資料的版面配置。 下表指出您可以用來定義屬性的資料類型和限定詞。 如需您可以使用的屬性和類別限定詞的詳細資訊，請參閱 [事件追蹤 MOF 限定詞](event-tracing-mof-qualifiers.md)。



| 資料類型              | 限定詞                        | 描述                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**、 **uint8**   | **格式**                        | 宣告1位元組的十進位整數。 若要宣告 ANSI 字元，請使用 **格式** 辨識符號，並將其值設定為 "c"。                                                                                                                                                                                                  |
| **sint16**、 **uint16** | **格式**                        | 宣告2個位元組的十進位整數。 若要指示數位是十六進位數位，請使用 **格式** 限定詞。 例如， ( "x" 格式 ) 。                                                                                                                                                                               |
| **sint32**、 **uint32** | **格式**                        | 宣告4位元組的十進位整數。 若要指示數位是十六進位數位，請使用 **格式** 辨識符號，並將其值設定為 "x"。                                                                                                                                                                                |
| **sint64**， **uint64** | **格式**                        | 宣告8位元組的十進位整數。 若要指示數位是十六進位數位，請使用 **格式** 辨識符號，並將其值設定為 "x"。                                                                                                                                                                                |
| **boolean**            |                                   | 宣告布林值。 事件取用者應該將值以 BOOL (4 位元組整數) 來解讀。                                                                                                                                                                                                                        |
| **char16**             |                                   | 宣告寬字元。 事件取用者應該將核心事件中的 char16 陣列轉譯為寬字元字串。  (使用陣列大小來複製字串。 某些字串可能會包含開頭的 Null 字元。 )                                                                                                       |
| **object**             | **分機**                     | 宣告二進位 blob。 **延伸** 模組辨識符號表示 blob 中的資料類型。                                                                                                                                                                                                                              |
| **string**             | **Format**、 **StringTermination** | 宣告字串值。 若要指出字串是寬字元字串，請使用 **格式** 辨識符號，並將其值設定為 "w"。 如果您未指定 **格式** 辨識符號，則字串會被視為 ANSI 字串。 若要指出字串的結束方式，請使用 **StringTermination** 限定詞。 <br/> |



 

若要指定陣列，您可以使用方括弧 \[ \] 。 方括弧可以包含陣列的大小。 例如：

`[WmiDataId(1), read] uint8 MyGuid[16];`

您也可以使用 **Max** 辨識符號來指定陣列的大小。 例如：

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

如果您在方括弧中包含陣列的大小，MOF 編譯器會為您產生最大限定詞。

請務必針對每個屬性使用 **描述** 限定詞。 描述應該包含取用者顯示內容值時可使用的顯示名稱。

下列範例會顯示描述提供者、事件和事件種類 MOF 類別之 MOF 檔案的內容。

``` syntax
#pragma namespace("\\\\.\\root\\wmi")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}")]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Class identifier"): Amended, read, Extension("Guid")] object ID;
};
```

請注意，提供者、事件和事件種類 MOF 類別名稱在整個命名空間中必須是唯一的。 若要避免命名衝突，您應該針對所有類別名稱使用唯一和描述性名稱。 類別屬性在其類別階層中也應該具有描述性和唯一的，也就是包含與父類別相同屬性名稱的子類別，會覆寫父類別的屬性。

定義您的 MOF 類別之後，請使用 MOF 編譯器來產生您的事件架構，並將它新增至 CIM 存放庫。 接著，取用者可以從存放庫讀取架構，並以程式設計方式讀取事件資料。 如需 MOF 語法和使用 MOF 編譯器 (Mofcomp.exe) 將 MOF 類別新增至 CIM 存放庫的完整說明，請參閱 [受控物件格式](../wmisdk/managed-object-format--mof-.md)。 如需使用 Wbemtest.exe 來存取 CIM 存放庫的詳細資訊，請參閱 [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI) 。

## <a name="versioning-mof-class"></a>版本設定 MOF 類別

如果您新增或變更事件種類 MOF 類別，則慣例是將事件 MOF 類別和其子事件種類 MOF 類別的版本設為版本。 若要將目前的事件 MOF 類別設為版本，請將 \_ Vn 附加至類別名稱，其中 n 是從0開始的遞增編號。 如果這是類別的第一個修訂，請將 \_ V0 附加至類別名稱。 您也必須將 **EventVersion** 限定詞新增至類別。 使用您在類別名稱中用來作為 **EventVersion** 限定詞值的相同版本號碼。

新版本的事件 MOF 類別必須使用與原始類別相同的名稱和 **Guid** 限定詞。 新的類別可以選擇性地新增 **EventVersion** 限定詞。 未包含 **EventVersion** 限定詞的事件 MOF 類別會被視為最新版本，或者，如果類別的所有版本都包含 **EventVersion** 辨識符號，則具有最高版本號碼的類別會被視為最新版本。 提供者會使用 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的 **類別. 版本** 成員，來識別追蹤中包含的事件版本。

下列範例示範如何為事件 MOF 類別的版本。

``` syntax
#pragma namespace("\\\\.\\root\\wmi")
#pragma classflags("forceupdate")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."),
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(1)]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1),
 EventName("MyEvent")]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
    [WmiDataId(6), Description("Buffer Size"): Amended, read] uint32 Size;
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(0)]
class MyCategory_V0 : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_V0_MyEvent : MyCategory_V0
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
};
```

 

 

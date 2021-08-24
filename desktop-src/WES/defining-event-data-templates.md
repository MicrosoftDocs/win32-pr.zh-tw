---
title: 定義事件資料範本
description: 提供者會使用資料範本來定義事件特定的資料，這些資料會包含在事件中，並定義當 ETW 追蹤會話啟用提供者時，可傳遞給提供者的篩選資料。
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5480ca158916801665943bd33b886bfcd5d73015e8730c1dd108123dadc1995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652608"
---
# <a name="defining-event-data-templates"></a>定義事件資料範本

提供者會使用資料範本來定義事件特定的資料，這些資料會包含在事件中，並定義當 ETW 追蹤會話啟用提供者時，可傳遞給提供者的篩選資料。 如果事件不包含事件特定的資料，您將不會定義範本。 若要定義範本，請使用 **範本** 元素。 範本包含提供者在事件中所包含之每個資料片段的資料項目。 您可以指定整數類資料類型、字串、陣列和結構。 您必須以範本中定義資料項目的順序來寫入事件資料。

您也可以包含範本中的 XML 片段，供取用者用來判斷如何呈現事件資料。 如果您未包含片段，取用者應該以範本中定義資料項目的順序轉譯事件資料。

當您定義範本時，您必須為它提供一個範本識別碼，您可以用它來參考事件定義中的範本。 範本中的每個資料項目都必須指定名稱和輸入資料類型 (針對輸入類型的清單，請參閱 [**InputType**](eventmanifestschema-inputtype-complextype.md) 複雜型別) 的 [備註] 區段。 如果可以使用多種格式來轉譯輸入資料類型，您應該指定輸出資料類型，告知取用者如何呈現資料項目。 例如，UInt32 輸入資料類型可以轉譯為不帶正負號的整數、執行緒識別碼、IPv4 位址和 Win32 錯誤碼。 如果您未指定輸出資料類型，取用者應該使用輸入類型的預設輸出類型來呈現資料項目。

若要指定陣列，請在資料項目上包含 **count** 屬性，並將它設定為數組中的元素數目。 陣列可以是變數大小陣列或固定大小陣列。 如果陣列是固定大小陣列，請將 [ **計數** ] 設定為數組的大小。 例如，如果整數陣列的大小固定為10，則將 [ **計數** ] 設定為10。 當您寫入陣列時，必須寫入40個位元組的資料。

如果陣列是變數大小陣列，請將 [ **計數** ] 設定為包含陣列大小的資料項目名稱。 如果陣列包含指標，指標的位址會以事件資料的形式寫入，而非指標指向的資料。

如果資料項目目是二進位 blob，您必須指定 **length** 屬性。 您也可以指定固定長度字串的 **length** 屬性。

如果資料項目代表列舉值，而且您想要取用者列印值的字串，而不是值本身，請指定 **對應** 屬性。

如果您在範本中包含結構，則應該個別撰寫結構的成員，而不是撰寫結構，除非您可以保證8位元組的界限對齊。

您應該仔細考慮事件中所包含的資訊，特別是當事件寫入至全域通道時。 一般來說，您不應該在事件中包含私用資訊。 這包括純文字密碼和個人使用者資訊。 此外，使用者所執行的程式、使用者造訪的 Url，以及與電腦上使用者活動相關的其他資訊，都應該視為私用。

如果您必須記錄事件中的 url 和使用者名稱，請勿將它們寫入 Windows 通道 (系統和應用程式) 因為所有已驗證的使用者都可以讀取這些通道。 相反地，請將它們寫入您自己的操作或分析通道。 設定這些通道上的存取權限，以僅允許系統管理員讀取事件。 您可能需要提供適當的洩漏，以通知使用者系統管理員可以使用私用資訊。

下列範例顯示如何定義範本。 您必須指定您在事件定義或篩選定義中參考的範本 **tid** 屬性。


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                <templates>
                    <template tid="t2">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>
                    </template>

                    <template tid="t3">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="ErrorCode" inType="win:Int32" outType="win:HResult"/>
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="BufferSize" inType="win:UInt32" />
                        <data name="Buffer" inType="win:Binary" length="BufferSize"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />
                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Value" inType="win:UInt16" />
                            <data name="Name" inType="win:UnicodeString" />
                        </struct>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

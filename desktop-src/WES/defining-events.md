---
title: 定義事件
description: 提供者必須定義它們撰寫的所有事件。 若要定義事件，請使用 event 元素。
ms.assetid: f282612c-cfa5-42fe-af8a-5b35c033abe2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4c1da0e54d1e9fc328978ebe447c8e843b540c
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104374876"
---
# <a name="defining-events"></a><span data-ttu-id="51584-104">定義事件</span><span class="sxs-lookup"><span data-stu-id="51584-104">Defining Events</span></span>

<span data-ttu-id="51584-105">提供者必須定義它們撰寫的所有事件。</span><span class="sxs-lookup"><span data-stu-id="51584-105">Providers must define all the events that they write.</span></span> <span data-ttu-id="51584-106">若要定義事件，請使用 **event** 元素。</span><span class="sxs-lookup"><span data-stu-id="51584-106">To define an event, use the **event** element.</span></span>

<span data-ttu-id="51584-107">**值** 屬性是事件識別碼，且必須是您定義之事件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="51584-107">The **value** attribute is the event identifier and it must be unique for the events that you define.</span></span> <span data-ttu-id="51584-108">您是否設定其他屬性，取決於將取用事件的人員和來源。</span><span class="sxs-lookup"><span data-stu-id="51584-108">Whether you set the other attributes depends on who will be consuming the events and from where.</span></span> <span data-ttu-id="51584-109">如果系統管理員將使用 Windows 事件檢視器之類的工具來取用您的事件，則您必須設定 **通道** 屬性。</span><span class="sxs-lookup"><span data-stu-id="51584-109">If administrators will be consuming your events using a tool like Windows Event Viewer, then you must set the **channel** attribute.</span></span> <span data-ttu-id="51584-110">如果通道類型為 Admin，則您也必須指定 **level** 屬性，並將它設定為 Winmeta.xml (Win： Critical 到 Win： Verbose) 中定義的其中一個層級。</span><span class="sxs-lookup"><span data-stu-id="51584-110">If the channel type is Admin, then you must also specify the **level** attribute and set it to one of the levels defined in Winmeta.xml (win:Critical through win:Verbose).</span></span>

<span data-ttu-id="51584-111">如果事件包含事件特定的資料，您必須將 **範本** 屬性設定為定義事件特定資料之範本的識別碼。</span><span class="sxs-lookup"><span data-stu-id="51584-111">If the event contains event-specific data, you must set the **template** attribute to the identifier of the template that defines the event-specific data.</span></span> <span data-ttu-id="51584-112">**層級**、**關鍵字**、**工作和** **opcode** 屬性是用來群組或值區事件。</span><span class="sxs-lookup"><span data-stu-id="51584-112">The **level**, **keywords**, **task**, and **opcode** attributes are used to group or bucket events.</span></span> <span data-ttu-id="51584-113">雖然這些屬性是選擇性的，但您應該考慮指定層級、工作、opcode 和關鍵字，讓取用者只能輕鬆存取感興趣的事件。</span><span class="sxs-lookup"><span data-stu-id="51584-113">Although these attributes are optional, you should consider specifying level, task, opcode, and keywords, so that consumers can easily access only those events of interest.</span></span> <span data-ttu-id="51584-114">ETW 追蹤會話也可以使用 **level** 和 **關鍵字** 屬性來限制寫入事件追蹤記錄檔的事件。</span><span class="sxs-lookup"><span data-stu-id="51584-114">The **level** and **keywords** attributes can also be used by an ETW tracing session to limit the events that are written to the event tracing log file.</span></span> <span data-ttu-id="51584-115">**關鍵字** 屬性包含以空格分隔的資訊清單中所定義的關鍵字名稱清單。</span><span class="sxs-lookup"><span data-stu-id="51584-115">The **keywords** attribute contains a space-delimited list of keyword names defined in the manifest.</span></span> <span data-ttu-id="51584-116">如果指定了多個關鍵字，它們的遮罩值會 OR'ed 在一起，以建立事件將使用的關鍵字值。</span><span class="sxs-lookup"><span data-stu-id="51584-116">If multiple keywords are specified their mask values are OR'ed together to create the keyword value that the event will use.</span></span>

<span data-ttu-id="51584-117">您應該設定 **符號** 屬性來指定編譯器所產生的符號常數，以識別事件的事件描述項-在寫入事件時，您會使用事件描述項。</span><span class="sxs-lookup"><span data-stu-id="51584-117">You should set the **symbol** attribute to specify the symbolic constant that the compiler generates to identify the event's event descriptor—you use the event descriptor when writing the event.</span></span> <span data-ttu-id="51584-118">如果您未指定符號，編譯器會為您產生名稱。</span><span class="sxs-lookup"><span data-stu-id="51584-118">If you do not specify the symbol, the compiler will generate a name for you.</span></span>

<span data-ttu-id="51584-119">**Message** 屬性包含與事件一起顯示的當地語系化訊息字串。</span><span class="sxs-lookup"><span data-stu-id="51584-119">The **message** attribute contains the localized message string that is displayed with the event.</span></span> <span data-ttu-id="51584-120">若要在字串中包含事件特定的資料，請在郵件內文中加入插入字串。</span><span class="sxs-lookup"><span data-stu-id="51584-120">To include event-specific data in the string, add insertion strings to the message text.</span></span> <span data-ttu-id="51584-121">例如，若要在範本中包含第三個數據項，請包含 %3。</span><span class="sxs-lookup"><span data-stu-id="51584-121">For example, to include the third data item in the template, include %3.</span></span>

<span data-ttu-id="51584-122">下列範例顯示定義事件的完整資訊清單。</span><span class="sxs-lookup"><span data-stu-id="51584-122">The following example shows a complete manifest that defines events.</span></span>

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

                <channels>
                    <importChannel chid="c1"
                                   name="Microsoft-Windows-BaseProvider/Admin"
                                   symbol="CHANNEL_BASEPROVIDER_ADMIN"
                                   />

                    <channel chid="c2"
                             name="Microsoft-Windows-SampleProvider/Operational"
                             type="Operational"
                             enabled="true"
                             />
                </channels>

                <levels>
                    <level name="NotValid"
                           value="16"
                           symbol="LEVEL_SAMPLEPROVIDER_NOTVALID"
                           message="$(string.Level.NotValid)"/>

                    <level name="Valid"
                           value="17"
                           symbol="LEVEL_SAMPLEPROVIDER_VALID"
                           message="$(string.Level.Valid)"/>
                </levels>

                <tasks>
                    <task name="Disconnect"
                          symbol="TASK_DISCONNECT"
                          value="1"
                          message="$(string.Task.Disconnect)"/>

                    <task name="Connect"
                          symbol="TASK_CONNECT"
                          value="2"
                          message="$(string.Task.Connect)"/>

                    <task name="Validate"
                          symbol="TASK_VALIDATE"
                          value="3"
                          message="$(string.Task.Validate)"/>
                </tasks>

                <opcodes>
                    <opcode name="Initialize"
                            symbol="OPCODE_INITIALIZE"
                            value="12"
                            message="$(string.Opcode.Initialize)"/>

                    <opcode name="Cleanup"
                            symbol="OPCODE_CLEANUP"
                            value="13"
                            message="$(string.Opcode.Cleanup)"/>
                 </opcodes>

                <keywords>
                    <keyword name="Read" mask="0x1" symbol="READ_KEYWORD"/>
                    <keyword name="Write" mask="0x2" symbol="WRITE_KEYWORD"/>
                    <keyword name="Local" mask="0x4" symbol="LOCAL_KEYWORD"/>
                    <keyword name="Remote" mask="0x8" symbol="REMOTE_KEYWORD"/>
                </keywords>

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

                    <template tid="t4">
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="Path" inType="win:UnicodeString" />
                    </template>
                </templates>

                <events>
                    <event value="1"
                        level="win:Informational"
                        keywords="Remote Read"
                        task="Connect"
                        template="t2"
                        channel="c1"
                        symbol="TRANSFER_SCHEDULE_EVENT"
                        message ="$(string.Event.XferSchedule)"/>

                    <event value="2"
                        level="win:Error"
                        keywords="Remote Write"
                        task="Disconnect"
                        opcode="Initialize"
                        template="t3"
                        channel="c1"
                        symbol="DOWNLOAD_XFER_FAILED_EVENT"
                        message ="$(string.Event.DownloadFailed)"/>

                    <event value="3"
                        level="NotValid"
                        keywords="Local Write"
                        task="Validate"
                        opcode="Cleanup"
                        template="t4"
                        channel="c2"
                        symbol="TEMPFILE_CLEANUP_EVENT"
                        message ="$(string.Event.TempFilesNotDeleted)"/>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Level.Valid" value="Valid"/>
                <string id="Level.NotValid" value="Not Valid"/>
                <string id="Task.Disconnect" value="Disconnect"/>
                <string id="Task.Connect" value="Connect"/>
                <string id="Task.Connect.ReadRegistry" value="ReadRegistry"/>
                <string id="Task.Validate" value="Connect"/>
                <string id="Task.Validate.GetRules" value="GetRules"/>
                <string id="Opcode.Initialize" value="Initialize"/>
                <string id="Opcode.Cleanup" value="Cleanup"/>
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
                <string id="Event.XferSchedule" value="The %1 %2 transfer will occur on %3."/>
                <string id="Event.DownloadFailed" value="The %1 download job failed with %2. The job contains the following files:%n%n%4"/>
                <string id="Event.TempFilesNotDeleted" value="The following temp files were not removed from %3:%n%n%2"/>
            </stringTable>
        </resources>
    </localization>
</instrumentationManifest>
```

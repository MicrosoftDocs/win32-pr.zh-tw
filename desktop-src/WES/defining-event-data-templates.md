---
title: 定義事件資料範本
description: 提供者會使用資料範本來定義事件特定的資料，這些資料會包含在事件中，並定義當 ETW 追蹤會話啟用提供者時，可傳遞給提供者的篩選資料。
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067230472c8de5ce29145e221c109b3f390f0a6c
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "103841980"
---
# <a name="defining-event-data-templates"></a><span data-ttu-id="aeaa8-103">定義事件資料範本</span><span class="sxs-lookup"><span data-stu-id="aeaa8-103">Defining Event Data Templates</span></span>

<span data-ttu-id="aeaa8-104">提供者會使用資料範本來定義事件特定的資料，這些資料會包含在事件中，並定義當 ETW 追蹤會話啟用提供者時，可傳遞給提供者的篩選資料。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-104">Providers use data templates to define the event-specific data that they include with an event and to define the filter data that an ETW tracing session can pass to the provider when it enables the provider.</span></span> <span data-ttu-id="aeaa8-105">如果事件不包含事件特定的資料，您將不會定義範本。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-105">If the event does not include event-specific data, you will not define a template.</span></span> <span data-ttu-id="aeaa8-106">若要定義範本，請使用 **範本** 元素。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-106">To define a template, use the **template** element.</span></span> <span data-ttu-id="aeaa8-107">範本包含提供者在事件中所包含之每個資料片段的資料項目。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-107">A template includes a data item for each piece of data that the provider includes with the event.</span></span> <span data-ttu-id="aeaa8-108">您可以指定整數類資料類型、字串、陣列和結構。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-108">You can specify integral types, strings, arrays, and structures.</span></span> <span data-ttu-id="aeaa8-109">您必須以範本中定義資料項目的順序來寫入事件資料。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-109">You must write the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="aeaa8-110">您也可以包含範本中的 XML 片段，供取用者用來判斷如何呈現事件資料。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-110">You can also include in the template, an XML fragment that consumers should use to determine how to render the event data.</span></span> <span data-ttu-id="aeaa8-111">如果您未包含片段，取用者應該以範本中定義資料項目的順序轉譯事件資料。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-111">If you do not include the fragment, consumers should render the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="aeaa8-112">當您定義範本時，您必須為它提供一個範本識別碼，您可以用它來參考事件定義中的範本。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-112">When you define a template, you must give it a template identifier that you use to reference the template in an event definition.</span></span> <span data-ttu-id="aeaa8-113">範本中的每個資料項目都必須指定名稱和輸入資料類型 (針對輸入類型的清單，請參閱 [**InputType**](eventmanifestschema-inputtype-complextype.md) 複雜型別) 的 [備註] 區段。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-113">Each data item in the template must specify a name and input data type (for a list of input types, see the Remarks section of the [**InputType**](eventmanifestschema-inputtype-complextype.md) complex type).</span></span> <span data-ttu-id="aeaa8-114">如果可以使用多種格式來轉譯輸入資料類型，您應該指定輸出資料類型，告知取用者如何呈現資料項目。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-114">If the input data type can be rendered in multiple formats, you should specify the output data type that tells consumers how to render the data item.</span></span> <span data-ttu-id="aeaa8-115">例如，UInt32 輸入資料類型可以轉譯為不帶正負號的整數、執行緒識別碼、IPv4 位址和 Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-115">For example, an UInt32 input data type can be rendered as an unsigned integer, thread identifier, IPv4 address, and Win32 error code among others.</span></span> <span data-ttu-id="aeaa8-116">如果您未指定輸出資料類型，取用者應該使用輸入類型的預設輸出類型來呈現資料項目。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-116">If you do not specify the output data type, consumers should use the input type's default output type to render the data item.</span></span>

<span data-ttu-id="aeaa8-117">若要指定陣列，請在資料項目上包含 **count** 屬性，並將它設定為數組中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-117">To specify an array, include the **count** attribute on the data item and set it to the number of elements in the array.</span></span> <span data-ttu-id="aeaa8-118">陣列可以是變數大小陣列或固定大小陣列。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-118">The array can be a variable size array or fixed size array.</span></span> <span data-ttu-id="aeaa8-119">如果陣列是固定大小陣列，請將 [ **計數** ] 設定為數組的大小。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-119">If the array is a fixed size array, set **count** to the size of the array.</span></span> <span data-ttu-id="aeaa8-120">例如，如果整數陣列的大小固定為10，則將 [ **計數** ] 設定為10。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-120">For example, if an array of integers has a fixed size of 10, set **count** to 10.</span></span> <span data-ttu-id="aeaa8-121">當您寫入陣列時，必須寫入40個位元組的資料。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-121">When you write the array, you must write 40 bytes of data.</span></span>

<span data-ttu-id="aeaa8-122">如果陣列是變數大小陣列，請將 [ **計數** ] 設定為包含陣列大小的資料項目名稱。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-122">If the array is a variable size array, set **count** to the name of the data item that contains the size of the array.</span></span> <span data-ttu-id="aeaa8-123">如果陣列包含指標，指標的位址會以事件資料的形式寫入，而非指標指向的資料。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-123">If the array contains pointers, the address of the pointers are written as the event data, not the data to which the pointers point.</span></span>

<span data-ttu-id="aeaa8-124">如果資料項目目是二進位 blob，您必須指定 **length** 屬性。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-124">You must specify the **length** attribute if the data item is a binary blob.</span></span> <span data-ttu-id="aeaa8-125">您也可以指定固定長度字串的 **length** 屬性。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-125">You can also specify the **length** attribute for fixed length strings.</span></span>

<span data-ttu-id="aeaa8-126">如果資料項目代表列舉值，而且您想要取用者列印值的字串，而不是值本身，請指定 **對應** 屬性。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-126">Specify the **map** attribute if the data item represents an enumeration value and you want the consumer to print a string for the value instead of the value itself.</span></span>

<span data-ttu-id="aeaa8-127">如果您在範本中包含結構，則應該個別撰寫結構的成員，而不是撰寫結構，除非您可以保證8位元組的界限對齊。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-127">If you include structures in the template, you should write the members of the structure individually instead of writing the structure unless you can guarantee 8-byte boundary alignment.</span></span>

<span data-ttu-id="aeaa8-128">您應該仔細考慮事件中所包含的資訊，特別是當事件寫入至全域通道時。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-128">You should carefully consider the information that you include in the events, especially when the events are written into the global channels.</span></span> <span data-ttu-id="aeaa8-129">一般來說，您不應該在事件中包含私用資訊。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-129">As a general rule, you should not include private information in the events.</span></span> <span data-ttu-id="aeaa8-130">這包括純文字密碼和個人使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-130">This includes plaintext passwords and personal user information.</span></span> <span data-ttu-id="aeaa8-131">此外，使用者所執行的程式、使用者造訪的 Url，以及與電腦上使用者活動相關的其他資訊，都應該視為私用。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-131">Additionally, programs run by the user, URLs that the user visited, and other information related to the user activities on the computer should be considered private.</span></span>

<span data-ttu-id="aeaa8-132">如果您必須記錄事件中的 Url 和使用者名稱，請勿將它們寫入 Windows 通道 (系統和應用程式) ，因為所有已驗證的使用者都可以讀取這些通道。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-132">If you must record URLs and user names in the events, do not write them to the Windows channels (System and Application) because these channels are readable by all authenticated users.</span></span> <span data-ttu-id="aeaa8-133">相反地，請將它們寫入您自己的操作或分析通道。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-133">Instead, write them to your own Operational or Analytic channels.</span></span> <span data-ttu-id="aeaa8-134">設定這些通道上的存取權限，以僅允許系統管理員讀取事件。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-134">Set the access permissions on these channels to allow only administrators to read the events.</span></span> <span data-ttu-id="aeaa8-135">您可能需要提供適當的洩漏，以通知使用者系統管理員可以使用私用資訊。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-135">You may need to provide an appropriate disclosure to notify users of the fact that private information is made available to the administrators.</span></span>

<span data-ttu-id="aeaa8-136">下列範例顯示如何定義範本。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-136">The following example shows how to define a template.</span></span> <span data-ttu-id="aeaa8-137">您必須指定您在事件定義或篩選定義中參考的範本 **tid** 屬性。</span><span class="sxs-lookup"><span data-stu-id="aeaa8-137">You must specify the template's **tid** attribute that you reference in the event definition or filter definition.</span></span>


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

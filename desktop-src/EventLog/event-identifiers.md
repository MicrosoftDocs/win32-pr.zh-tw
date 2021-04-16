---
description: 事件識別碼可唯一識別特定的事件。
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: '事件記錄 (事件識別碼) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402337cb2c7e862785a88ec604c6382152736fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512176"
---
# <a name="event-identifiers-event-logging"></a><span data-ttu-id="2cbc7-103">事件記錄 (事件識別碼) </span><span class="sxs-lookup"><span data-stu-id="2cbc7-103">Event Identifiers (Event Logging)</span></span>

<span data-ttu-id="2cbc7-104">事件識別碼可唯一識別特定的事件。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-104">Event identifiers uniquely identify a particular event.</span></span> <span data-ttu-id="2cbc7-105">每個 [事件來源](event-sources.md) 都可以定義自己的編號事件，以及它們在其訊息檔案中對應的描述字串。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-105">Each [event source](event-sources.md) can define its own numbered events and the description strings to which they are mapped in its message file.</span></span> <span data-ttu-id="2cbc7-106">事件檢視器可將這些字串呈現給使用者。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-106">Event viewers can present these strings to the user.</span></span> <span data-ttu-id="2cbc7-107">他們應該可以協助使用者瞭解發生什麼問題，並建議要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-107">They should help the user understand what went wrong and suggest what actions to take.</span></span> <span data-ttu-id="2cbc7-108">引導使用者解決自己的問題，而不是在系統管理員或支援技術人員上的說明。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-108">Direct the description at users solving their own problems, not at administrators or support technicians.</span></span> <span data-ttu-id="2cbc7-109">如需詳細資訊，請參閱 [錯誤訊息指導方針](/windows/desktop/Debug/error-message-guidelines)。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-109">For more information, see [Error Message Guidelines](/windows/desktop/Debug/error-message-guidelines).</span></span>

## <a name="format"></a><span data-ttu-id="2cbc7-110">格式</span><span class="sxs-lookup"><span data-stu-id="2cbc7-110">Format</span></span>

<span data-ttu-id="2cbc7-111">下圖說明事件識別碼的格式。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-111">The following diagram illustrates the format of an event identifier.</span></span>

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span data-ttu-id="2cbc7-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>嚴重性</span><span class="sxs-lookup"><span data-stu-id="2cbc7-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev</span></span>
</dt> <dd>

<span data-ttu-id="2cbc7-113">嚴重性。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-113">Severity.</span></span> <span data-ttu-id="2cbc7-114">嚴重性的定義如下：</span><span class="sxs-lookup"><span data-stu-id="2cbc7-114">The severity is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="2cbc7-115">00-成功</span><span class="sxs-lookup"><span data-stu-id="2cbc7-115">00 - Success</span></span></dd> <dd><span data-ttu-id="2cbc7-116">01-資訊</span><span class="sxs-lookup"><span data-stu-id="2cbc7-116">01 - Informational</span></span></dd> <dd><span data-ttu-id="2cbc7-117">10-警告</span><span class="sxs-lookup"><span data-stu-id="2cbc7-117">10 - Warning</span></span></dd> <dd><span data-ttu-id="2cbc7-118">11-錯誤</span><span class="sxs-lookup"><span data-stu-id="2cbc7-118">11 - Error</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="2cbc7-119"><span id="C"></span><span id="c"></span>C</span><span class="sxs-lookup"><span data-stu-id="2cbc7-119"><span id="C"></span><span id="c"></span>C</span></span>
</dt> <dd>

<span data-ttu-id="2cbc7-120">客戶位。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-120">Customer bit.</span></span> <span data-ttu-id="2cbc7-121">此位定義如下：</span><span class="sxs-lookup"><span data-stu-id="2cbc7-121">This bit is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="2cbc7-122">0-系統程式碼</span><span class="sxs-lookup"><span data-stu-id="2cbc7-122">0 - System code</span></span></dd> <dd><span data-ttu-id="2cbc7-123">1-客戶程式碼</span><span class="sxs-lookup"><span data-stu-id="2cbc7-123">1 - Customer code</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="2cbc7-124"><span id="R"></span><span id="r"></span>R</span><span class="sxs-lookup"><span data-stu-id="2cbc7-124"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="2cbc7-125">保留位元 </span><span class="sxs-lookup"><span data-stu-id="2cbc7-125">Reserved bit.</span></span>

</dd> <dt>

<span data-ttu-id="2cbc7-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>設施</span><span class="sxs-lookup"><span data-stu-id="2cbc7-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Facility</span></span>
</dt> <dd>

<span data-ttu-id="2cbc7-127">設備碼。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-127">Facility code.</span></span> <span data-ttu-id="2cbc7-128">此值可以是設備 \_ Null。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-128">This value can be FACILITY\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="2cbc7-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼</span><span class="sxs-lookup"><span data-stu-id="2cbc7-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

<span data-ttu-id="2cbc7-130">設備的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-130">Status code for the facility.</span></span>

</dd> </dl>

## <a name="message-definitions"></a><span data-ttu-id="2cbc7-131">訊息定義</span><span class="sxs-lookup"><span data-stu-id="2cbc7-131">Message Definitions</span></span>

<span data-ttu-id="2cbc7-132">訊息是在事件訊息檔案中定義。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-132">Messages are defined in the event message file.</span></span> <span data-ttu-id="2cbc7-133">事件訊息檔中的描述字串是依事件識別碼進行編制索引，讓事件檢視器根據事件識別碼顯示任何事件的事件特定文字。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-133">The description strings in the event message file are indexed by event identifier, enabling Event Viewer to display event-specific text for any event based on the event identifier.</span></span> <span data-ttu-id="2cbc7-134">所有描述都具有當地語系化和語言相依。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-134">All descriptions are localized and language dependent.</span></span> <span data-ttu-id="2cbc7-135">如需建立訊息檔案的詳細資訊，請參閱 [訊息文字檔](message-text-files.md)。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-135">For more information on building a message file, see [Message Text Files](message-text-files.md).</span></span>

<span data-ttu-id="2cbc7-136">描述字串可能包含%*n* 形式的插入字串預留位置，其中 %1 表示第一個插入字串，依此類推。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-136">The description strings may contain insertion string placeholders, of the form %*n*, where %1 indicates the first insertion string, and so on.</span></span> <span data-ttu-id="2cbc7-137">例如，以下是在 mc 檔案中的範例專案：</span><span class="sxs-lookup"><span data-stu-id="2cbc7-137">For example, the following is a sample entry in the .mc file:</span></span>

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

<span data-ttu-id="2cbc7-138">在此情況下， [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) 所傳回的緩衝區會包含插入字串。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-138">In this case, the buffer returned by [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contains insertion strings.</span></span> <span data-ttu-id="2cbc7-139">[**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord)結構的 **NumStrings** 成員表示插入字串的數目。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-139">The **NumStrings** member of the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure indicates the number of insertion strings.</span></span> <span data-ttu-id="2cbc7-140">**EVENTLOGRECORD** 結構的 **StringOffset** 成員表示緩衝區中第一個插入字串的位置。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-140">The **StringOffset** member of the **EVENTLOGRECORD** structure indicates the location of the first insertion string in the buffer.</span></span> <span data-ttu-id="2cbc7-141">您可以傳遞 DWORD \_ PTRs 的陣列，這個陣列會在呼叫 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 函式時，指向緩衝區中每個字串的位址，並將字串插入訊息中。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-141">You can pass an array of DWORD\_PTRs that point to the address each string in the buffer when calling the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function and it will insert the strings into the message.</span></span>

<span data-ttu-id="2cbc7-142">描述字串也可以包含參數訊息檔案中參數字串的預留位置。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-142">The description string can also contain placeholders for parameter strings from the parameter message file.</span></span> <span data-ttu-id="2cbc7-143">預留位置的格式為%%*n*，其中% %1 取代為識別碼為1的參數字串，依此類推。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-143">The placeholders are of the form %%*n*, where %%1 is replaced by the parameter string with the identifier of 1, and so on.</span></span> <span data-ttu-id="2cbc7-144">不過，您必須將參數字串插入 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 傳回的訊息字串中。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-144">However, it is up to you to insert the parameter strings into the message string that [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) returns.</span></span> <span data-ttu-id="2cbc7-145">一般來說，您會呼叫 **FormatMessage** 來取得事件的訊息字串。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-145">Typically, you call **FormatMessage** to get the message string for the event.</span></span> <span data-ttu-id="2cbc7-146">然後，您可以剖析%%*n* 參數的訊息字串。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-146">You then parse the message string for %%*n* parameters.</span></span> <span data-ttu-id="2cbc7-147">如果訊息包含一或多個參數，請載入來源的 **ParameterMessageFile** 登錄值。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-147">If the message contains one or more parameters, load the **ParameterMessageFile** registry value for the source.</span></span> <span data-ttu-id="2cbc7-148">針對訊息字串中的每個參數，取得識別碼，並將它傳遞給 **FormatMessage** 以取得參數字串。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-148">For each parameter in the message string, get the identifier and pass it to **FormatMessage** to get the parameter string.</span></span> <span data-ttu-id="2cbc7-149">將訊息字串中的參數取代為 **FormatMessage** 傳回的參數字串。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-149">Replace the parameter in the message string with the parameter string that **FormatMessage** returned.</span></span>

## <a name="insertion-strings"></a><span data-ttu-id="2cbc7-150">插入字串</span><span class="sxs-lookup"><span data-stu-id="2cbc7-150">Insertion Strings</span></span>

<span data-ttu-id="2cbc7-151">插入字串是選擇性的語言獨立字串，用來填入描述字串中的預留位置值。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-151">Insertion strings are optional language-independent strings used to fill in values for placeholders in description strings.</span></span> <span data-ttu-id="2cbc7-152">因為字串未當地語系化，所以這些預留位置只能用來表示與語言無關的字串，例如數值、檔案名、使用者名稱等等。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-152">Because the strings are not localized, it is critical that these placeholders be used only to represent language-independent strings such as numeric values, file names, user names, and so on.</span></span> <span data-ttu-id="2cbc7-153">字串長度不能超過 32 kb-1 個字元。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-153">The string length must not exceed 32 kilobytes - 1 characters.</span></span>

<span data-ttu-id="2cbc7-154">請避免使用數個字串來建立較大的描述。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-154">Avoid using several strings to create a larger description.</span></span> <span data-ttu-id="2cbc7-155">插入字串應該被視為資料，而不是文字。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-155">An insertion string should be treated as data, not text.</span></span> <span data-ttu-id="2cbc7-156">例如，在下列範例中，不應該使用 pszString1 和 pszString2 做為 pszDescription 的插入字串。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-156">For example, in the following example, pszString1 and pszString2 should not be used as insertion strings for pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

<span data-ttu-id="2cbc7-157">在下列範例中，您適合使用 pszString1 或 pszString2 在 pszDescription 中插入字串。</span><span class="sxs-lookup"><span data-stu-id="2cbc7-157">In the following example, it is appropriate to use either pszString1 or pszString2 for the insertion string in pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 

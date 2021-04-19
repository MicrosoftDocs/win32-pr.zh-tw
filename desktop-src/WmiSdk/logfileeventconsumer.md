---
description: 當事件傳遞至文字記錄檔時，LogFileEventConsumer 類別會將自訂字串寫入至文字記錄檔。
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: LogFileEventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 462989b740aaf6a6bd78968c951b7c676038cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974217"
---
# <a name="logfileeventconsumer-class"></a><span data-ttu-id="3eb1c-103">LogFileEventConsumer 類別</span><span class="sxs-lookup"><span data-stu-id="3eb1c-103">LogFileEventConsumer class</span></span>

<span data-ttu-id="3eb1c-104">當事件傳遞至文字記錄檔時， **LogFileEventConsumer** 類別會將自訂字串寫入至文字記錄檔。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-104">The **LogFileEventConsumer** class writes customized strings to a text log file when events are delivered to it.</span></span> <span data-ttu-id="3eb1c-105">這些字串會以行尾序列分隔。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-105">The strings are separated by end-of-line sequences.</span></span> <span data-ttu-id="3eb1c-106">此類別是 WMI 提供的其中一個標準事件取用者。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-106">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="3eb1c-107">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3eb1c-108">語法</span><span class="sxs-lookup"><span data-stu-id="3eb1c-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a><span data-ttu-id="3eb1c-109">成員</span><span class="sxs-lookup"><span data-stu-id="3eb1c-109">Members</span></span>

<span data-ttu-id="3eb1c-110">**LogFileEventConsumer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3eb1c-110">The **LogFileEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="3eb1c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3eb1c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3eb1c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="3eb1c-112">Properties</span></span>

<span data-ttu-id="3eb1c-113">**LogFileEventConsumer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-113">The **LogFileEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3eb1c-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eb1c-115">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="3eb1c-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3eb1c-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3eb1c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eb1c-117">安全識別碼 (SID) ，可唯一識別建立篩選的使用者。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="3eb1c-118">根據作業系統而定，WMI 會儲存建立 [**\_ \_ EventConsumer**](--eventconsumer.md)實例或系統管理員 SID 之使用者的 SID。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-118">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="3eb1c-119">如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="3eb1c-120">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-120">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eb1c-121">**檔案名稱**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-121">**Filename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eb1c-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eb1c-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3eb1c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eb1c-124">檔案的名稱，其中包含附加記錄專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-124">Name of a file that includes the path to which the log entries are appended.</span></span> <span data-ttu-id="3eb1c-125">如果檔案不存在， **LogFileEventConsumer** 會嘗試建立它。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-125">If the file does not exist, **LogFileEventConsumer** attempts to create it.</span></span> <span data-ttu-id="3eb1c-126">當路徑不存在，或建立取用者的使用者沒有檔案或路徑的寫入權限時，取用者會失敗。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-126">The consumer fails when the path does not exist, or when the user who creates the consumer does not have write permissions for the file or path.</span></span>

</dd> <dt>

<span data-ttu-id="3eb1c-127">**IsUnicode**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-127">**IsUnicode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eb1c-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3eb1c-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3eb1c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eb1c-130">若 **為 TRUE**，則表示記錄檔是 Unicode 文字檔。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-130">If **TRUE**, the log file is a Unicode text file.</span></span> <span data-ttu-id="3eb1c-131">如果 **為 FALSE**，則表示記錄檔是多位元組程式碼文字檔。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-131">If **FALSE**, the log file is a multibyte code text file.</span></span> <span data-ttu-id="3eb1c-132">如果檔案存在，則會忽略此屬性，並使用目前的檔案設定。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-132">If the file exists, this property is ignored and the current file setting is used.</span></span> <span data-ttu-id="3eb1c-133">例如，如果 **IsUnicode** 為 **FALSE**，但現有的檔案是 unicode 檔案，則會使用 unicode。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-133">For example, if **IsUnicode** is **FALSE**, but the existing file is a Unicode file, then Unicode is used.</span></span> <span data-ttu-id="3eb1c-134">如果 **IsUnicode** 為 **TRUE**，但檔案是多位元組程式碼，則會使用多位元組程式碼。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-134">If **IsUnicode** is **TRUE**, but the file is multibyte code, then multibyte code is used.</span></span>

</dd> <dt>

<span data-ttu-id="3eb1c-135">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-135">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eb1c-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eb1c-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3eb1c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eb1c-138">Windows Management Instrumentation (WMI) 傳送事件的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-138">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="3eb1c-139">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-139">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eb1c-140">**MaximumFileSize**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-140">**MaximumFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eb1c-141">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3eb1c-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3eb1c-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eb1c-143">記錄檔的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-143">Maximum size of a log file in bytes.</span></span> <span data-ttu-id="3eb1c-144">如果主要檔案超過其大小上限，則會將內容移至不同的檔案，並清空主要檔案。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-144">If the primary file exceeds its maximum size, the contents are moved to a different file and the primary file is emptied.</span></span> <span data-ttu-id="3eb1c-145">值為 0 (零) 表示沒有大小限制。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-145">A value of 0 (zero) means there is no size limit.</span></span> <span data-ttu-id="3eb1c-146">預設值為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-146">The default value is 65,535 bytes.</span></span> <span data-ttu-id="3eb1c-147">在寫入作業之前，會檢查檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-147">The size of the file is checked before a write operation.</span></span> <span data-ttu-id="3eb1c-148">因此，您可以有稍微大於指定大小限制的檔案。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-148">Therefore, you can have a file that is slightly larger than the specified size limit.</span></span> <span data-ttu-id="3eb1c-149">下一次寫入作業會攔截它，並啟動新的檔案。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-149">The next write operation catches it and starts a new file.</span></span>

<span data-ttu-id="3eb1c-150">下列清單會識別備份檔案的命名結構：</span><span class="sxs-lookup"><span data-stu-id="3eb1c-150">The following list identifies the naming structure for the backup file:</span></span>

-   <span data-ttu-id="3eb1c-151">如果原始檔案名為8.3，則會使用 "001"、"002" 格式的字串來取代此延伸模組，依此類推，其最小數位會大於所有先前使用和選擇的數位。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-151">If the original filename is 8.3, the extension is replaced by a string in the format of "001", "002", and so on with the smallest number larger than all the previously used and chosen numbers.</span></span> <span data-ttu-id="3eb1c-152">如果使用 "999"，則選擇的數位是最小未使用的數位。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-152">If "999" is used, then the number chosen is the smallest unused number.</span></span>
-   <span data-ttu-id="3eb1c-153">如果原始檔案名不是8.3，則會在檔案名後面附加 "001"、"002" 等格式的字串。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-153">If the original filename is not 8.3, a string in the format of "001", "002", and so on is appended to the file name.</span></span>

<span data-ttu-id="3eb1c-154">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3eb1c-155">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-155">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eb1c-156">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3eb1c-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3eb1c-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eb1c-158">特定取用者的佇列上限，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-158">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="3eb1c-159">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-159">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eb1c-160">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eb1c-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eb1c-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3eb1c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eb1c-163">限定詞：索引 [**鍵**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="3eb1c-163">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="3eb1c-164">此取用者的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-164">Unique name for this consumer.</span></span>

</dd> <dt>

<span data-ttu-id="3eb1c-165">**Text**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-165">**Text**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eb1c-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eb1c-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3eb1c-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eb1c-168">記錄專案文字的標準字串 [範本](using-standard-string-templates.md) 。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-168">Standard string [template](using-standard-string-templates.md) for the text of a log entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3eb1c-169">備註</span><span class="sxs-lookup"><span data-stu-id="3eb1c-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3eb1c-170">**LogFileEventConsumer** 不會保護記錄檔。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-170">The **LogFileEventConsumer** does not secure the log file.</span></span> <span data-ttu-id="3eb1c-171">因此，當您設定 **LogFileEventConsumer** 時，請務必指定受限於所需層級的目錄。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-171">Therefore, when you configure the **LogFileEventConsumer**, it is important to specify a directory that is secured to the level that you require.</span></span>

 

<span data-ttu-id="3eb1c-172">**LogFileEventConsumer** 類別衍生自 [**\_ \_ EventConsumer**](--eventconsumer.md)抽象類別。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-172">The **LogFileEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="3eb1c-173">範例</span><span class="sxs-lookup"><span data-stu-id="3eb1c-173">Examples</span></span>

<span data-ttu-id="3eb1c-174">如需使用 **LogFileEventConsumer** 來建立取用者的範例，請參閱 [根據事件寫入記錄](writing-to-a-log-file-based-on-an-event.md)檔。</span><span class="sxs-lookup"><span data-stu-id="3eb1c-174">For an example of using **LogFileEventConsumer** to create a consumer, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3eb1c-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="3eb1c-175">Requirements</span></span>



| <span data-ttu-id="3eb1c-176">需求</span><span class="sxs-lookup"><span data-stu-id="3eb1c-176">Requirement</span></span> | <span data-ttu-id="3eb1c-177">值</span><span class="sxs-lookup"><span data-stu-id="3eb1c-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3eb1c-178">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3eb1c-178">Minimum supported client</span></span><br/> | <span data-ttu-id="3eb1c-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eb1c-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3eb1c-180">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3eb1c-180">Minimum supported server</span></span><br/> | <span data-ttu-id="3eb1c-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3eb1c-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3eb1c-182">命名空間</span><span class="sxs-lookup"><span data-stu-id="3eb1c-182">Namespace</span></span><br/>                | <span data-ttu-id="3eb1c-183">根 \\ 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="3eb1c-183">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="3eb1c-184">MOF</span><span class="sxs-lookup"><span data-stu-id="3eb1c-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3eb1c-185"><dt>Wbemcons mof</dt></span><span class="sxs-lookup"><span data-stu-id="3eb1c-185"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="3eb1c-186">DLL</span><span class="sxs-lookup"><span data-stu-id="3eb1c-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3eb1c-187"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3eb1c-187"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eb1c-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3eb1c-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eb1c-189">標準取用者類別</span><span class="sxs-lookup"><span data-stu-id="3eb1c-189">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="3eb1c-190">根據事件寫入記錄檔</span><span class="sxs-lookup"><span data-stu-id="3eb1c-190">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="3eb1c-191">建立邏輯取用者</span><span class="sxs-lookup"><span data-stu-id="3eb1c-191">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="3eb1c-192">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="3eb1c-192">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="3eb1c-193">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="3eb1c-193">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 


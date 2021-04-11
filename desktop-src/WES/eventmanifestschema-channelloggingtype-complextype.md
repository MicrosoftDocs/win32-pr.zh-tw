---
title: ChannelLoggingType 複雜類型
description: 定義支援通道之記錄檔的屬性，例如其容量，以及是否為連續或迴圈。 |ChannelLoggingType 複雜類型
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- ChannelLoggingType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cfaf6dfa225799befcd0c7fb068c0f779ea33eb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104116153"
---
# <a name="channelloggingtype-complex-type"></a><span data-ttu-id="11e22-105">ChannelLoggingType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="11e22-105">ChannelLoggingType Complex Type</span></span>

<span data-ttu-id="11e22-106">定義支援通道之記錄檔的屬性，例如其容量，以及是否為連續或迴圈。</span><span class="sxs-lookup"><span data-stu-id="11e22-106">Defines the properties of the log file that backs the channel, such as its capacity and whether it is sequential or circular.</span></span>

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="11e22-107">子元素</span><span class="sxs-lookup"><span data-stu-id="11e22-107">Child elements</span></span>



| <span data-ttu-id="11e22-108">元素</span><span class="sxs-lookup"><span data-stu-id="11e22-108">Element</span></span>                                                                         | <span data-ttu-id="11e22-109">類型</span><span class="sxs-lookup"><span data-stu-id="11e22-109">Type</span></span>                                                              | <span data-ttu-id="11e22-110">Description</span><span class="sxs-lookup"><span data-stu-id="11e22-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11e22-111">**autoBackup**</span><span class="sxs-lookup"><span data-stu-id="11e22-111">**autoBackup**</span></span>](eventmanifestschema-autobackup-channelloggingtype-element.md) | <span data-ttu-id="11e22-112">boolean</span><span class="sxs-lookup"><span data-stu-id="11e22-112">boolean</span></span>                                                           | <span data-ttu-id="11e22-113">決定當目前的記錄檔達到大小上限時，是否要建立新的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="11e22-113">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span> <span data-ttu-id="11e22-114">設定為 **true** ，要求服務在記錄檔達到其大小上限時，建立新的檔案;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="11e22-114">Set to **true** to request that the service create a new file when the log file reaches its maximum size; otherwise, **false**.</span></span> <span data-ttu-id="11e22-115">只有當 [[**保留**](eventmanifestschema-retention-channelloggingtype-element.md)] 設定為 [ **true**] 時，才可以將 [**autoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md)設定為 [ **true** ]。</span><span class="sxs-lookup"><span data-stu-id="11e22-115">You can set [**autoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) to **true** only if [**retention**](eventmanifestschema-retention-channelloggingtype-element.md) is set to **true**.</span></span> <span data-ttu-id="11e22-116">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="11e22-116">The default is **false**.</span></span><br/> <span data-ttu-id="11e22-117">服務可以建立的備份檔案數目沒有限制 (只有) 可用磁碟空間的限制。</span><span class="sxs-lookup"><span data-stu-id="11e22-117">There is no limit to the number of backup files that the service can create (limited only by available disk space).</span></span> <span data-ttu-id="11e22-118">備份檔案名稱的形式為 Archive-*channelName* - *timestamp*，而且位於% windir% \\ System32 \\ \system32\winevt\logs\application.evtx \\ Logs 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="11e22-118">The backup file names are of the form Archive-*channelName*-*timestamp*.evtx and are located in %windir%\\System32\\winevt\\Logs folder.</span></span><br/> |
| [<span data-ttu-id="11e22-119">**maxSize**</span><span class="sxs-lookup"><span data-stu-id="11e22-119">**maxSize**</span></span>](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [<span data-ttu-id="11e22-120">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="11e22-120">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="11e22-121">記錄檔的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="11e22-121">The maximum size, in bytes, of the log file.</span></span> <span data-ttu-id="11e22-122">預設的 (和最小) 值是 1 MB。</span><span class="sxs-lookup"><span data-stu-id="11e22-122">The default (and minimum) value is 1 MB.</span></span> <span data-ttu-id="11e22-123">如果實體記錄檔大小小於設定的最大大小，且記錄檔中需要額外的空間來儲存事件，則即使記錄檔的實際大小將大於設定的最大值，服務仍會配置另一個空間區塊。</span><span class="sxs-lookup"><span data-stu-id="11e22-123">If the physical log size is less than the configured maximum size and additional space is required in the log to store events, the service will allocate another block of space even if the resulting physical size of the log will be larger than the configured maximum size.</span></span> <span data-ttu-id="11e22-124">服務會配置 1 MB 的區塊，因此實體大小可成長到大於設定之大小上限的 1 MB。</span><span class="sxs-lookup"><span data-stu-id="11e22-124">The service allocates blocks of 1 MB so the physical size could grow to up to 1 MB larger than the configured max size.</span></span> <br/>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="11e22-125">**保留**</span><span class="sxs-lookup"><span data-stu-id="11e22-125">**retention**</span></span>](eventmanifestschema-retention-channelloggingtype-element.md)   | <span data-ttu-id="11e22-126">boolean</span><span class="sxs-lookup"><span data-stu-id="11e22-126">boolean</span></span>                                                           | <span data-ttu-id="11e22-127">判斷記錄檔是否為連續或迴圈的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="11e22-127">Determines whether the log file is a sequential or circular log file.</span></span> <span data-ttu-id="11e22-128">針對連續記錄檔將設定為 **true** ，並將迴圈記錄檔設為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="11e22-128">Set to **true** for a sequential log file and **false** for a circular log file.</span></span> <span data-ttu-id="11e22-129">系統管理員和操作通道類型的預設值為 **false** ，而針對分析和 Debug 通道類型則為 **true** 。</span><span class="sxs-lookup"><span data-stu-id="11e22-129">The default is **false** for Admin and Operational channel types and **true** for Analytic and Debug channel types.</span></span><br/> <span data-ttu-id="11e22-130">若要查詢迴圈記錄檔，您必須先停用通道。</span><span class="sxs-lookup"><span data-stu-id="11e22-130">To query a circular log, you must first disable the channel.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="11e22-131">備註</span><span class="sxs-lookup"><span data-stu-id="11e22-131">Remarks</span></span>

<span data-ttu-id="11e22-132">您可以為任何通道類型指定 **maxSize** 屬性。</span><span class="sxs-lookup"><span data-stu-id="11e22-132">You can specify the **maxSize** attribute for any channel type.</span></span>

<span data-ttu-id="11e22-133">您只能針對系統管理員和操作通道類型指定 **autoBackup** 屬性。</span><span class="sxs-lookup"><span data-stu-id="11e22-133">You can specify the **autoBackup** attribute only for Admin and Operational channel types.</span></span>

<span data-ttu-id="11e22-134">您可以將 [ **保留** ] 屬性設定為 false (系統管理員和操作通道類型的迴圈記錄) 。</span><span class="sxs-lookup"><span data-stu-id="11e22-134">You can set the **retention** attribute to false (circular logging) for Admin and Operational channel types.</span></span> <span data-ttu-id="11e22-135">您可以將 [ **保留** ] 屬性設定為 False (分析和 Debug 通道類型的迴圈記錄) ，但若要在 Windows 事件檢視器中查看事件，您必須先停用通道。</span><span class="sxs-lookup"><span data-stu-id="11e22-135">You can set the **retention** attribute to false (circular logging) for Analytic and Debug channel types but to view the events in the Windows Event Viewer, you will need to first disable the channel.</span></span> <span data-ttu-id="11e22-136">請注意，當您再次啟用通道時，會從通道中移除事件。</span><span class="sxs-lookup"><span data-stu-id="11e22-136">Note that when you enable the channel again, the events are removed from the channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="11e22-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="11e22-137">Requirements</span></span>



| <span data-ttu-id="11e22-138">需求</span><span class="sxs-lookup"><span data-stu-id="11e22-138">Requirement</span></span> | <span data-ttu-id="11e22-139">值</span><span class="sxs-lookup"><span data-stu-id="11e22-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="11e22-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11e22-140">Minimum supported client</span></span><br/> | <span data-ttu-id="11e22-141">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11e22-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="11e22-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11e22-142">Minimum supported server</span></span><br/> | <span data-ttu-id="11e22-143">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11e22-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






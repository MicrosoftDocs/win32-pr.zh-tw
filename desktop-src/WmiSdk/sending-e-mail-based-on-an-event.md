---
description: 藉由使用 SMTPEventConsumer 類別，您可以在發生指定事件時，將電子郵件傳送給指定的使用者。 此類別是 WMI 提供的標準事件取用者。
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: 根據事件傳送電子郵件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4929b7c8c29d514d73a6e4c9d14049a19f306233
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980896"
---
# <a name="sending-email-based-on-an-event"></a><span data-ttu-id="b2fac-104">根據事件傳送電子郵件</span><span class="sxs-lookup"><span data-stu-id="b2fac-104">Sending Email Based on an Event</span></span>

<span data-ttu-id="b2fac-105">藉由使用 [SMTPEventConsumer](smtpeventconsumer.md) 類別，您可以在發生指定事件時，將電子郵件傳送給指定的使用者。</span><span class="sxs-lookup"><span data-stu-id="b2fac-105">By using the [SMTPEventConsumer](smtpeventconsumer.md) class, you can send email to a designated user when a specified event occurs.</span></span> <span data-ttu-id="b2fac-106">此類別是 WMI 提供的 [標準事件取用者](standard-consumer-classes.md) 。</span><span class="sxs-lookup"><span data-stu-id="b2fac-106">This class is a [standard event consumer](standard-consumer-classes.md) that WMI provides.</span></span>

<span data-ttu-id="b2fac-107">[SMTPEventConsumer](smtpeventconsumer.md)類別需要下列條件，才能傳送電子郵件訊息以回應事件：</span><span class="sxs-lookup"><span data-stu-id="b2fac-107">The [SMTPEventConsumer](smtpeventconsumer.md) class requires the following conditions to send an email message in response to an event:</span></span>

-   <span data-ttu-id="b2fac-108">[SMTPEventConsumer](smtpeventconsumer.md)類別必須編譯成正確的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b2fac-108">The [SMTPEventConsumer](smtpeventconsumer.md) class must be compiled into the correct namespace.</span></span> <span data-ttu-id="b2fac-109">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="b2fac-109">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>
-   <span data-ttu-id="b2fac-110">SMTP 伺服器必須存在於網路上。</span><span class="sxs-lookup"><span data-stu-id="b2fac-110">An SMTP server must exist on the network.</span></span>
-   <span data-ttu-id="b2fac-111">電子郵件訊息不能有附件。</span><span class="sxs-lookup"><span data-stu-id="b2fac-111">The email message cannot have an attachment.</span></span>
-   <span data-ttu-id="b2fac-112">電子郵件訊息必須以 US-ASCII 編碼。</span><span class="sxs-lookup"><span data-stu-id="b2fac-112">The email message must be encoded in US-ASCII.</span></span>

<span data-ttu-id="b2fac-113">使用標準取用者的基本程式一律相同，且位於 [監視和回應標準取用者的事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="b2fac-113">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="b2fac-114">下列程式會新增至基本程式;是 [SMTPEventConsumer](smtpeventconsumer.md) 類別特有的;並描述如何建立傳送電子郵件的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="b2fac-114">The following procedure adds to the basic procedure; is specific to the [SMTPEventConsumer](smtpeventconsumer.md) class; and describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="b2fac-115">下列程式描述如何建立傳送電子郵件的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="b2fac-115">The following procedure describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="b2fac-116">**建立傳送電子郵件的事件取用者**</span><span class="sxs-lookup"><span data-stu-id="b2fac-116">**To create an event consumer that sends email**</span></span>

1.  <span data-ttu-id="b2fac-117">如有必要，請安裝並註冊 [SMTPEventConsumer](smtpeventconsumer.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="b2fac-117">Install and register the [SMTPEventConsumer](smtpeventconsumer.md) class, if necessary.</span></span>

    <span data-ttu-id="b2fac-118">WMI 安裝程式會將 [SMTPEventConsumer](smtpeventconsumer.md) 類別編譯為根 \\ 訂用帳戶命名空間。</span><span class="sxs-lookup"><span data-stu-id="b2fac-118">The [SMTPEventConsumer](smtpeventconsumer.md) class is compiled into the root\\subscription namespace by the WMI setup program.</span></span>

2.  <span data-ttu-id="b2fac-119">找出您想要監視的事件，並建立事件查詢。</span><span class="sxs-lookup"><span data-stu-id="b2fac-119">Identify the event that you want to monitor and create the event query.</span></span>

    <span data-ttu-id="b2fac-120">可能會有用來監視事件的現有內部事件。</span><span class="sxs-lookup"><span data-stu-id="b2fac-120">There might be an existing intrinsic event that use to monitor your event.</span></span> <span data-ttu-id="b2fac-121">大部分內建事件都與 "root \\ cimv2" 命名空間中的類別實例變更相關聯。</span><span class="sxs-lookup"><span data-stu-id="b2fac-121">Most intrinsic events are associated with changes to class instances in the "root\\cimv2" namespace.</span></span> <span data-ttu-id="b2fac-122">藉由分析 [WMI 類別](wmi-classes.md) 參考中的類別，您可能會找到可識別您要監視之事件的類別。</span><span class="sxs-lookup"><span data-stu-id="b2fac-122">By analyzing the classes in the [WMI Classes](wmi-classes.md) reference, you can probably find a class that identifies the event you want to monitor.</span></span> <span data-ttu-id="b2fac-123">例如，使用 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別來監視硬碟的變更。</span><span class="sxs-lookup"><span data-stu-id="b2fac-123">For example, use the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class to monitor changes to a hard disk drive.</span></span>

    <span data-ttu-id="b2fac-124">如果沒有任何現有的內部事件使用，可能會有可運作的外來事件提供者。</span><span class="sxs-lookup"><span data-stu-id="b2fac-124">If there are no existing intrinsic events that use, there might be an extrinsic event provider that can work.</span></span> <span data-ttu-id="b2fac-125">例如，使用登錄提供者的 [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) 類別來監視系統登錄的變更。</span><span class="sxs-lookup"><span data-stu-id="b2fac-125">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="b2fac-126">如果找不到識別您要監視之事件的類別，您必須建立自己的事件提供者，並定義新的外建事件類別。</span><span class="sxs-lookup"><span data-stu-id="b2fac-126">If a class does not exist that identifies the event you want to monitor, you must create your own event provider and define new extrinsic event classes.</span></span> <span data-ttu-id="b2fac-127">如需詳細資訊，請參閱 [撰寫事件提供者](writing-an-event-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="b2fac-127">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

3.  <span data-ttu-id="b2fac-128">在受控物件格式 (MOF) 檔中，建立 [SMTPEventConsumer](smtpeventconsumer.md) 的實例以接收事件。</span><span class="sxs-lookup"><span data-stu-id="b2fac-128">In the Managed Object Format (MOF) file, create an instance of the [SMTPEventConsumer](smtpeventconsumer.md) to receive events.</span></span>

    <span data-ttu-id="b2fac-129">您可以使用實例的屬性，定義事件發生時要傳送的電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="b2fac-129">Use the properties of the instance to define the email message to send when an event occurs.</span></span> <span data-ttu-id="b2fac-130">例如， **ToLine** 屬性會定義電子郵件地址，而 **Message** 屬性則會定義電子郵件訊息的文字。</span><span class="sxs-lookup"><span data-stu-id="b2fac-130">For example, the **ToLine** property defines the email address, and the **Message** property defines the text of the email message.</span></span> <span data-ttu-id="b2fac-131">您必須定義電子郵件地址、主旨和訊息的文字，但是電子郵件訊息不能有附件。</span><span class="sxs-lookup"><span data-stu-id="b2fac-131">You must define the email address, subject, and text of a message, but an email message cannot have an attachment.</span></span> <span data-ttu-id="b2fac-132">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="b2fac-132">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

4.  <span data-ttu-id="b2fac-133">建立指定您要監視之事件的事件查詢。</span><span class="sxs-lookup"><span data-stu-id="b2fac-133">Create an event query that specifies the events you want to monitor.</span></span>

    <span data-ttu-id="b2fac-134">如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="b2fac-134">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

5.  <span data-ttu-id="b2fac-135">建立 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，並將您的查詢儲存在 **查詢** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="b2fac-135">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and store your query in the **Query** property.</span></span>

    <span data-ttu-id="b2fac-136">如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="b2fac-136">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

6.  <span data-ttu-id="b2fac-137">建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以建立篩選和取用者的關聯。</span><span class="sxs-lookup"><span data-stu-id="b2fac-137">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer.</span></span>
7.  <span data-ttu-id="b2fac-138">使用 [**Mofcomp.exe**](mofcomp.md)編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="b2fac-138">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>


## <a name="example"></a><span data-ttu-id="b2fac-139">範例</span><span class="sxs-lookup"><span data-stu-id="b2fac-139">Example</span></span>

<span data-ttu-id="b2fac-140">本節中的範例是在 MOF 程式碼中，但您可以使用 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md) 或 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立實例。</span><span class="sxs-lookup"><span data-stu-id="b2fac-140">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="b2fac-141">下列程式說明如何使用範例。</span><span class="sxs-lookup"><span data-stu-id="b2fac-141">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="b2fac-142">**使用範例**</span><span class="sxs-lookup"><span data-stu-id="b2fac-142">**To use the example**</span></span>

1.  <span data-ttu-id="b2fac-143">將下列 MOF 複製到文字檔，並以 MOF 副檔名儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="b2fac-143">Copy the following MOF to a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="b2fac-144">在 [命令提示字元] 視窗中，使用下列命令編譯 MOF 檔案：</span><span class="sxs-lookup"><span data-stu-id="b2fac-144">In a command prompt window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="b2fac-145">**Mofcomp.exe** *filename \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="b2fac-145">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

> [!Note]  
> <span data-ttu-id="b2fac-146">當 MOF 程式碼編譯為根訂用帳戶 \\ 命名空間時， [SMTPEventConsumer](smtpeventconsumer.md) 會編譯成相同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b2fac-146">When MOF code is compiled into the root\\subscription namespace, the [SMTPEventConsumer](smtpeventconsumer.md) is compiled into the same namespace.</span></span>

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a><span data-ttu-id="b2fac-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2fac-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2fac-148">使用標準取用者監視及回應事件</span><span class="sxs-lookup"><span data-stu-id="b2fac-148">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 

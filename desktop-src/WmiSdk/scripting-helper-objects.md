---
description: WMI 有數個腳本 helper 物件，可提供腳本所需的轉換。
ms.assetid: 832660b7-2992-4d1f-af16-7b8f0477b187
ms.tgt_platform: multiple
title: 腳本 Helper 物件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 028079e49a2007d99b81f7832c4bce3cb016701d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974380"
---
# <a name="scripting-helper-objects"></a><span data-ttu-id="12b56-103">腳本 Helper 物件</span><span class="sxs-lookup"><span data-stu-id="12b56-103">Scripting Helper Objects</span></span>

<span data-ttu-id="12b56-104">WMI 有數個腳本 helper 物件，可提供腳本所需的轉換。</span><span class="sxs-lookup"><span data-stu-id="12b56-104">WMI has several scripting helper objects that supply the conversions required by scripts.</span></span>

<span data-ttu-id="12b56-105">WMI 腳本 helper 物件包括：</span><span class="sxs-lookup"><span data-stu-id="12b56-105">WMI scripting helper objects include:</span></span>

-   [<span data-ttu-id="12b56-106">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="12b56-106">**SWbemDateTime**</span></span>](swbemdatetime.md)
-   [<span data-ttu-id="12b56-107">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="12b56-107">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
-   [<span data-ttu-id="12b56-108">**Win32 \_ SecurityDescriptorHelper**</span><span class="sxs-lookup"><span data-stu-id="12b56-108">**Win32\_SecurityDescriptorHelper**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)

<span data-ttu-id="12b56-109">Helper 物件會細分複合資料結構，因此不需要腳本來剖析結構以取得任何片段。</span><span class="sxs-lookup"><span data-stu-id="12b56-109">The helper objects break down composite data structures so that a script is not required to parse the structure to obtain any of the pieces.</span></span> <span data-ttu-id="12b56-110">例如， **WMI DATETIME** 結構無法直接顯示，與其他 Windows DATETIME 資料結構（例如 **VT \_ DATE**）不同。</span><span class="sxs-lookup"><span data-stu-id="12b56-110">For example, the **WMI DATETIME** structure cannot be displayed directly, and is different from other Windows datetime data structures, such as **VT\_DATE**.</span></span>

## <a name="swbemdatetime"></a><span data-ttu-id="12b56-111">SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="12b56-111">SWbemDateTime</span></span>

<span data-ttu-id="12b56-112">[**SWbemDateTime**](swbemdatetime.md)物件提供的屬性會剖析出日、月、年、一天中的時間等等。</span><span class="sxs-lookup"><span data-stu-id="12b56-112">The [**SWbemDateTime**](swbemdatetime.md) object provides properties that parse out the day, month, year, time of day, and so on.</span></span> <span data-ttu-id="12b56-113">它也提供轉換方法，以將 Windows Management Instrumentation (WMI) datetime 轉換成 **VT \_ 日期** 和 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 格式。</span><span class="sxs-lookup"><span data-stu-id="12b56-113">It also provides conversion methods to convert the Windows Management Instrumentation (WMI) datetime to and from the **VT\_Date** and [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) formats.</span></span> <span data-ttu-id="12b56-114">針對 Internet Explorer (IE) 安全性設定， **SWbemDateTime** 物件是唯一標示為 safe 以進行初始化的 WMI 腳本物件，以及可安全的腳本處理。</span><span class="sxs-lookup"><span data-stu-id="12b56-114">For Internet Explorer (IE) security settings, the **SWbemDateTime** object is the only WMI scripting object that is marked safe for initialization and safe for scripting.</span></span> <span data-ttu-id="12b56-115">如需日期和時間轉換的詳細資訊和範例，請參閱有關「日期 [和](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) 時間」以及有關 TechNet ScriptCenter 的文章，也就 [是 (喔的時間，以及日期的) ](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx)。</span><span class="sxs-lookup"><span data-stu-id="12b56-115">For more information and examples of date and time conversions, see [Dates and Times](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) and the article on TechNet ScriptCenter [It's About Time (Oh, and About Dates, too)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span></span>

## <a name="swbemobjectpath"></a><span data-ttu-id="12b56-116">SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="12b56-116">SWbemObjectPath</span></span>

<span data-ttu-id="12b56-117">[**SWbemObjectPath**](swbemobjectpath.md)的屬性提供物件的絕對路徑，但也會細分 WMI 路徑的部分，例如伺服器、命名空間、類別或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="12b56-117">The properties of [**SWbemObjectPath**](swbemobjectpath.md) supply the absolute path of an object, but also break out the parts of the WMI path, such as server, namespace, class, or relative path.</span></span> <span data-ttu-id="12b56-118">物件可讓您設定路徑的安全性、取得代表路徑之物件的索引鍵值、判斷物件是否為 singleton，依此類推。</span><span class="sxs-lookup"><span data-stu-id="12b56-118">The object allows you to set the security of the path, obtain the key values of the objects representing the path, determine if an object is a singleton, and so on.</span></span> <span data-ttu-id="12b56-119">如需使用 WMI 物件路徑的詳細資訊，請參閱 [描述 Wmi 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="12b56-119">For more information about working with WMI object paths, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

## <a name="win32_securitydescriptorhelper"></a><span data-ttu-id="12b56-120">Win32 \_ SecurityDescriptorHelper</span><span class="sxs-lookup"><span data-stu-id="12b56-120">Win32\_SecurityDescriptorHelper</span></span>

<span data-ttu-id="12b56-121">[**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)類別會將安全物件的安全描述項從某種格式轉換成另一種格式。</span><span class="sxs-lookup"><span data-stu-id="12b56-121">The [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class converts the security descriptor of a securable object from one format to another.</span></span>

<span data-ttu-id="12b56-122">許多物件（例如印表機、WMI 命名空間、登錄機碼或 DCOM 應用程式）都有安全描述項可控制物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="12b56-122">Many objects, such as printers, WMI namespaces, registry keys, or DCOM applications, have security descriptors that control access to the object.</span></span> <span data-ttu-id="12b56-123">您可以藉由取得或設定與物件相關聯的安全描述項，使用 WMI 來探索或變更可存取這些物件的人員。</span><span class="sxs-lookup"><span data-stu-id="12b56-123">You can use WMI to discover or change who has access to these objects by getting or setting the security descriptor associated with the object.</span></span>

<span data-ttu-id="12b56-124">不過，不同的方法可能會取得二進位位元組陣列中的安全描述項、 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-string-format) (SDDL) 格式，或作為 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)的實例。</span><span class="sxs-lookup"><span data-stu-id="12b56-124">However, different methods may obtain security descriptors in a binary byte array, [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-string-format) (SDDL) format, or as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="12b56-125">除了針對 [安全描述項作業](/windows/desktop/SecAuthZ/security-descriptor-operations)而設計的 c + + 方法以外，不應操作安全描述項的二進位位元組陣列形式。</span><span class="sxs-lookup"><span data-stu-id="12b56-125">The binary byte array form of a security descriptor should not be manipulated except by the C++ methods designed for [Security Descriptor Operations](/windows/desktop/SecAuthZ/security-descriptor-operations).</span></span> <span data-ttu-id="12b56-126">SDDL 中的描述元是在字串中，但仍很難操作。</span><span class="sxs-lookup"><span data-stu-id="12b56-126">Descriptors in SDDL are in strings, but are still awkward to manipulate.</span></span> <span data-ttu-id="12b56-127">最簡單的操作格式是 **Win32 \_ SecurityDescriptor**，因為它包含信任者、ACE 和 SID 的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="12b56-127">The easiest format to manipulate is **Win32\_SecurityDescriptor**, because it contains embedded objects for trustee, ACE, and SID.</span></span> <span data-ttu-id="12b56-128">如需 WMI 中安全描述項結構的詳細資訊，請參閱 [Wmi 安全描述項物件](wmi-security-descriptor-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="12b56-128">For more information about the structure of security descriptors in WMI, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).</span></span> <span data-ttu-id="12b56-129">如需如何進行轉換的詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="12b56-129">For more information about how to do conversions, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12b56-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="12b56-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12b56-131">WMI 中的腳本</span><span class="sxs-lookup"><span data-stu-id="12b56-131">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 

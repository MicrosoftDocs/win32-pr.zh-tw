---
description: 您可以藉由連線至 WMI，然後呼叫 CreateObject，在 Visual Basic Scripting Edition (VBScript) 中建立 WMI 的物件。 下表列出支持對象建立之 WMI 的腳本 API 中的方法。
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: 使用 VBScript 建立物件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469264"
---
# <a name="creating-an-object-using-vbscript"></a><span data-ttu-id="aec4d-104">使用 VBScript 建立物件</span><span class="sxs-lookup"><span data-stu-id="aec4d-104">Creating an Object Using VBScript</span></span>

<span data-ttu-id="aec4d-105">您可以藉由連線至 WMI，然後呼叫 [CreateObject](/previous-versions//xzysf6hc(v=vs.85))，在 Visual Basic Scripting Edition (VBScript) 中建立 WMI 的物件。</span><span class="sxs-lookup"><span data-stu-id="aec4d-105">You can create an object for WMI in Visual Basic Scripting Edition (VBScript) by connecting to WMI and then calling [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span> <span data-ttu-id="aec4d-106">下表列出支持對象建立之 WMI 的腳本 API 中的方法。</span><span class="sxs-lookup"><span data-stu-id="aec4d-106">The following table lists the methods in the Scripting API for WMI that support object creation.</span></span>



| <span data-ttu-id="aec4d-107">介面</span><span class="sxs-lookup"><span data-stu-id="aec4d-107">Interface</span></span>                                        | <span data-ttu-id="aec4d-108">ProgID</span><span class="sxs-lookup"><span data-stu-id="aec4d-108">ProgID</span></span>                             |
|--------------------------------------------------|------------------------------------|
| [<span data-ttu-id="aec4d-109">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="aec4d-109">**SWbemDateTime**</span></span>](swbemdatetime.md)           | <span data-ttu-id="aec4d-110">"WbemScripting.SwbemDateTime"</span><span class="sxs-lookup"><span data-stu-id="aec4d-110">"WbemScripting.SwbemDateTime"</span></span>      |
| [<span data-ttu-id="aec4d-111">**Wbemscripting.swbemlocator**</span><span class="sxs-lookup"><span data-stu-id="aec4d-111">**SWbemLocator**</span></span>](swbemlocator.md)             | <span data-ttu-id="aec4d-112">"WbemScripting. Wbemscripting.swbemlocator"</span><span class="sxs-lookup"><span data-stu-id="aec4d-112">"WbemScripting.SWbemLocator"</span></span>       |
| [<span data-ttu-id="aec4d-113">**SWbemLastError**</span><span class="sxs-lookup"><span data-stu-id="aec4d-113">**SWbemLastError**</span></span>](swbemlasterror.md)         | <span data-ttu-id="aec4d-114">"WbemScripting. SWbem. LastError"</span><span class="sxs-lookup"><span data-stu-id="aec4d-114">"WbemScripting.SWbem.LastError"</span></span>    |
| [<span data-ttu-id="aec4d-115">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="aec4d-115">**SWbemObjectPath**</span></span>](swbemobjectpath.md)       | <span data-ttu-id="aec4d-116">"WbemScripting.SWbemObjectPath"</span><span class="sxs-lookup"><span data-stu-id="aec4d-116">"WbemScripting.SWbemObjectPath"</span></span>    |
| [<span data-ttu-id="aec4d-117">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="aec4d-117">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md) | <span data-ttu-id="aec4d-118">"WbemScripting.SWbemNamedValueSet"</span><span class="sxs-lookup"><span data-stu-id="aec4d-118">"WbemScripting.SWbemNamedValueSet"</span></span> |
| [<span data-ttu-id="aec4d-119">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="aec4d-119">**SWbemRefresher**</span></span>](swbemrefresher.md)         | <span data-ttu-id="aec4d-120">"WbemScripting.SWbemRefresher"</span><span class="sxs-lookup"><span data-stu-id="aec4d-120">"WbemScripting.SWbemRefresher"</span></span>     |
| [<span data-ttu-id="aec4d-121">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="aec4d-121">**SWbemSink**</span></span>](swbemsink.md)                   | <span data-ttu-id="aec4d-122">"WbemScripting. SWbemSink"</span><span class="sxs-lookup"><span data-stu-id="aec4d-122">"WbemScripting.SWbemSink"</span></span>          |



 

<span data-ttu-id="aec4d-123">下列程式描述如何使用 VBScript 建立 WMI 物件。</span><span class="sxs-lookup"><span data-stu-id="aec4d-123">The following procedure describes how to create a WMI object using VBScript.</span></span>

<span data-ttu-id="aec4d-124">**使用 VBScript 建立 WMI 物件**</span><span class="sxs-lookup"><span data-stu-id="aec4d-124">**To create a WMI object using VBScript**</span></span>

1.  <span data-ttu-id="aec4d-125">使用名字或 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件連接至 WMI。</span><span class="sxs-lookup"><span data-stu-id="aec4d-125">Connect to WMI using either a moniker or an [**SWbemLocator**](swbemlocator.md) object.</span></span>

    <span data-ttu-id="aec4d-126">如需詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="aec4d-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

2.  <span data-ttu-id="aec4d-127">對 VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 方法進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="aec4d-127">Make a call to the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method.</span></span>

    <span data-ttu-id="aec4d-128">下列程式碼範例顯示如何建立物件。</span><span class="sxs-lookup"><span data-stu-id="aec4d-128">The following code example shows how to create an object.</span></span>

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    <span data-ttu-id="aec4d-129">如果您在步驟1中使用了標記，就不需要再次呼叫 [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="aec4d-129">If you use a moniker in Step 1, you do not need to call [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) again.</span></span>

 

 

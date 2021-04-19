---
description: 邏輯取用者是永久事件取用者類別的實例。
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: 建立邏輯取用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcbd62f2eee57a9e254d5700344d7b8da414469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983868"
---
# <a name="creating-a-logical-consumer"></a><span data-ttu-id="89d3c-103">建立邏輯取用者</span><span class="sxs-lookup"><span data-stu-id="89d3c-103">Creating a Logical Consumer</span></span>

<span data-ttu-id="89d3c-104">邏輯取用者是永久事件取用者類別的實例。</span><span class="sxs-lookup"><span data-stu-id="89d3c-104">A logical consumer is an instance of a permanent event consumer class.</span></span> <span data-ttu-id="89d3c-105">邏輯取用者的主要目的是為實體取用者提供實體取用者所執行活動的參數。</span><span class="sxs-lookup"><span data-stu-id="89d3c-105">The main purpose of a logical consumer is to provide the physical consumer with the parameters for the activities the physical consumer performs.</span></span> <span data-ttu-id="89d3c-106">如需詳細資訊，請參閱 [建立新的永久事件取用者類別](creating-a-new-permanent-event-consumer-class.md)。</span><span class="sxs-lookup"><span data-stu-id="89d3c-106">For more information, see [Creating a New Permanent Event Consumer Class](creating-a-new-permanent-event-consumer-class.md).</span></span> <span data-ttu-id="89d3c-107">永久取用者在取用者、篩選和系結實例中必須具有相同的 [**CreatorSID**](--eventconsumer.md) 。</span><span class="sxs-lookup"><span data-stu-id="89d3c-107">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="89d3c-108">如需詳細資訊，請參閱 [安全地接收事件](receiving-events-securely.md)。</span><span class="sxs-lookup"><span data-stu-id="89d3c-108">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span> <span data-ttu-id="89d3c-109">如需使用邏輯取用者的範例，請參閱 [根據事件執行腳本](running-a-script-based-on-an-event.md)，它會顯示使用標準取用者類別 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 來設定永久取用者。</span><span class="sxs-lookup"><span data-stu-id="89d3c-109">For an example of using a logical consumer, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md), which shows the use of the standard consumer class [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to configure a permanent consumer.</span></span>

<span data-ttu-id="89d3c-110">下列程式說明如何建立邏輯取用者。</span><span class="sxs-lookup"><span data-stu-id="89d3c-110">The following procedure describes how to create a logical consumer.</span></span>

<span data-ttu-id="89d3c-111">**建立邏輯取用者**</span><span class="sxs-lookup"><span data-stu-id="89d3c-111">**To create a logical consumer**</span></span>

1.  <span data-ttu-id="89d3c-112">建立永久取用者類別的實例。</span><span class="sxs-lookup"><span data-stu-id="89d3c-112">Create an instance of your permanent consumer class.</span></span>
2.  <span data-ttu-id="89d3c-113">使用您想要實體取用者執行之動作的參數，填滿實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="89d3c-113">Fill the properties of the instance with the parameters of the action you want the physical consumer to perform.</span></span>

<span data-ttu-id="89d3c-114">下列 MOF 程式碼範例說明包含腳本的邏輯取用者。</span><span class="sxs-lookup"><span data-stu-id="89d3c-114">The following MOF code example describes a logical consumer that contains a script.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $CONSUMER
{
    Name = "MyConsumerName";
    ScriptingEngine = "VBScript";
    ScriptText = 

        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\\\ASEC.log\", 8, true);\n"
        "objFile.WriteLine \"Time: \" + new Date() + \";\n"
        "objFile.WriteLine \"Entry made by: \\\"ActiveScript\\\"\";\n"
        "objFile.Close\n";
    
    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="89d3c-115">建立邏輯取用者之後，您必須將每個篩選準則連結至事件篩選器，以將動作指派給特定的事件。</span><span class="sxs-lookup"><span data-stu-id="89d3c-115">After you create the logical consumer, you must then link each filter to an event filter to assign the action to a particular event.</span></span> <span data-ttu-id="89d3c-116">如需詳細資訊，請參閱 [建立事件篩選](creating-an-event-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="89d3c-116">For more information, see [Creating an Event Filter](creating-an-event-filter.md).</span></span>

 

 




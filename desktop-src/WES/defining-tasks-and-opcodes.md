---
title: 定義工作和作業碼
description: 提供者會使用工作和操作碼以邏輯方式分組事件。 群組事件可協助取用者只查詢包含特定工作和作業碼組合的事件。
ms.assetid: 6a872517-14de-423e-a7ff-7edb9a29b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257166a34c167d076fec39ac6997d12dc785450
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104507849"
---
# <a name="defining-tasks-and-opcodes"></a><span data-ttu-id="d9552-104">定義工作和作業碼</span><span class="sxs-lookup"><span data-stu-id="d9552-104">Defining Tasks and Opcodes</span></span>

<span data-ttu-id="d9552-105">提供者會使用工作和操作碼以邏輯方式分組事件。</span><span class="sxs-lookup"><span data-stu-id="d9552-105">Providers use tasks and opcodes to logically group events.</span></span> <span data-ttu-id="d9552-106">群組事件可協助取用者只查詢包含特定工作和作業碼組合的事件。</span><span class="sxs-lookup"><span data-stu-id="d9552-106">Grouping events helps consumers query for only those events that contain specific task and opcode combinations.</span></span> <span data-ttu-id="d9552-107">一般而言，您會使用工作來識別提供者的主要元件，例如網路或資料庫元件。</span><span class="sxs-lookup"><span data-stu-id="d9552-107">Typically, you use tasks to identify a major component of the provider such as the networking or database component.</span></span> <span data-ttu-id="d9552-108">然後，您可以使用操作碼來識別元件執行的作業，例如網路元件的傳送和接收作業。</span><span class="sxs-lookup"><span data-stu-id="d9552-108">You could then use opcodes to identify the operations that the component performs, such as the send and receive operations for a networking component.</span></span> <span data-ttu-id="d9552-109">如果您只有一個元件，則可以使用 [工作] 反映元件中的主要作業，例如 [連接] 或 [中斷連接]，然後使用 opcode 來反映作業內的活動，例如讀取登錄。</span><span class="sxs-lookup"><span data-stu-id="d9552-109">If you had only one component, you could use task to reflect a major operation in the component, such as connect or disconnect, and use opcode to reflect an activity within the operation such as reading the registry.</span></span> <span data-ttu-id="d9552-110">您也可以在不指定工作的情況下使用操作碼。</span><span class="sxs-lookup"><span data-stu-id="d9552-110">You could also use opcode without specifying a task.</span></span> <span data-ttu-id="d9552-111">您可以使用工作和操作碼來分組取用者的事件，完全由您決定。</span><span class="sxs-lookup"><span data-stu-id="d9552-111">How you use task and opcodes to group events for the consumer is completely up to you.</span></span>

<span data-ttu-id="d9552-112">若要定義工作，請使用 **task** 元素。</span><span class="sxs-lookup"><span data-stu-id="d9552-112">To define a task, use the **task** element.</span></span> <span data-ttu-id="d9552-113">若要定義作業碼，請使用 **opcode** 元素。</span><span class="sxs-lookup"><span data-stu-id="d9552-113">To define an opcode, use the **opcode** element.</span></span> <span data-ttu-id="d9552-114">您最多可以指定228碼。</span><span class="sxs-lookup"><span data-stu-id="d9552-114">You can specify up to 228 opcodes.</span></span> <span data-ttu-id="d9552-115">工作 **值** 必須大於0。</span><span class="sxs-lookup"><span data-stu-id="d9552-115">The task **value** must be greater than 0.</span></span> <span data-ttu-id="d9552-116">Opcode 的範圍必須在11到239之間。</span><span class="sxs-lookup"><span data-stu-id="d9552-116">The opcodes must be in the range from 11 through 239.</span></span> <span data-ttu-id="d9552-117">Winmeta.xml 的檔案會定義您可以使用的一般作業，而不是定義您自己的作業。</span><span class="sxs-lookup"><span data-stu-id="d9552-117">The Winmeta.xml file defines common operations that you can use instead of defining your own.</span></span>

<span data-ttu-id="d9552-118">下列範例將示範如何定義數個工作和操作碼。</span><span class="sxs-lookup"><span data-stu-id="d9552-118">The following example shows how to define several tasks and opcodes.</span></span>

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

                <tasks>
                    <task name="Disconnect" 
                          symbol="TASK_DISCONNECT"
                          value="1"
                          message="$(string.Task.Disconnect)"/>
 
                    <task name="Connect" 
                          symbol="TASK_CONNECT"
                          value="2"
                          message="$(string.Task.Connect)">
                    </task>

                    <task name="Validate" 
                          symbol="TASK_VALIDATE"
                          value="3"
                          message="$(string.Task.Validate)">
                    </task>
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

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Task.Disconnect" value="Disconnect"/>
                <string id="Task.Connect" value="Connect"/>
                <string id="Task.Connect.ReadRegistry" value="ReadRegistry"/>
                <string id="Task.Validate" value="Connect"/>
                <string id="Task.Validate.GetRules" value="GetRules"/>
                <string id="Opcode.Initialize" value="Initialize"/>
                <string id="Opcode.Cleanup" value="Cleanup"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

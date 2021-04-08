---
title: MCI 命令字串和訊息
description: MCI 命令字串和訊息
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- MCI 命令字串，關於
- MCI 命令訊息，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a317442280b8fb4c7afe7832205b1c7128513
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842300"
---
# <a name="mci-command-strings-and-messages"></a><span data-ttu-id="672cf-105">MCI 命令字串和訊息</span><span class="sxs-lookup"><span data-stu-id="672cf-105">MCI Command Strings and Messages</span></span>

<span data-ttu-id="672cf-106">MCI 支援 [命令字串](command-strings.md) 和 [命令訊息](command-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="672cf-106">MCI supports [Command Strings](command-strings.md) and [Command Messages](command-messages.md).</span></span> <span data-ttu-id="672cf-107">您可以在 MCI 應用程式中使用字串或訊息，或兩者。</span><span class="sxs-lookup"><span data-stu-id="672cf-107">You can use either strings or messages, or both, in your MCI application.</span></span>

-   <span data-ttu-id="672cf-108">*命令訊息介面* 包含常數和結構。</span><span class="sxs-lookup"><span data-stu-id="672cf-108">The *command-message interface* consists of constants and structures.</span></span> <span data-ttu-id="672cf-109">使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式，將訊息傳送至 MCI 裝置。</span><span class="sxs-lookup"><span data-stu-id="672cf-109">Use the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send messages to an MCI device.</span></span>
-   <span data-ttu-id="672cf-110">*命令字串介面* 提供命令訊息的文字版本。</span><span class="sxs-lookup"><span data-stu-id="672cf-110">The *command-string interface* provides a textual version of the command messages.</span></span> <span data-ttu-id="672cf-111">使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式將字串傳送至 MCI 裝置。</span><span class="sxs-lookup"><span data-stu-id="672cf-111">Use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function to send strings to an MCI device.</span></span> <span data-ttu-id="672cf-112">命令字串會複製命令訊息的功能。</span><span class="sxs-lookup"><span data-stu-id="672cf-112">Command strings duplicate the functionality of the command messages.</span></span> <span data-ttu-id="672cf-113">作業系統會先將命令字串轉換成命令訊息，然後再將它們傳送至 MCI 驅動程式進行處理。</span><span class="sxs-lookup"><span data-stu-id="672cf-113">The operating system converts the command strings to command messages before sending them to the MCI driver for processing.</span></span>

<span data-ttu-id="672cf-114">取得資訊的命令訊息會以結構的形式來進行，在 C 應用程式中很容易解讀。</span><span class="sxs-lookup"><span data-stu-id="672cf-114">The command messages that retrieve information do so in the form of structures, which are easy to interpret in a C application.</span></span> <span data-ttu-id="672cf-115">這些結構可以包含裝置許多不同層面的資訊。</span><span class="sxs-lookup"><span data-stu-id="672cf-115">These structures can contain information on many different aspects of a device.</span></span> <span data-ttu-id="672cf-116">取得資訊的命令字串會以字串形式來進行，而且一次只能取出一個字串。</span><span class="sxs-lookup"><span data-stu-id="672cf-116">The command strings that retrieve information do so in the form of strings, and can only retrieve one string at a time.</span></span> <span data-ttu-id="672cf-117">您的應用程式必須剖析或測試每個字串才能加以解讀。</span><span class="sxs-lookup"><span data-stu-id="672cf-117">Your application must parse or test each string to interpret it.</span></span> <span data-ttu-id="672cf-118">在某些情況下，您可能會發現命令訊息比命令字串更容易使用，但命令字串很容易記住和實行。</span><span class="sxs-lookup"><span data-stu-id="672cf-118">You might find that the command messages are easier to use than the command strings in some cases, but the command strings are easy to remember and implement.</span></span> <span data-ttu-id="672cf-119">某些 MCI 應用程式會在傳回值不會使用時使用命令字串 (除了用來驗證從裝置取得資訊時的成功) 和命令訊息。</span><span class="sxs-lookup"><span data-stu-id="672cf-119">Some MCI applications use command strings when the return value will not be used (other than to verify success) and command messages when retrieving information from the device.</span></span>

<span data-ttu-id="672cf-120">當您討論到命令時，此總覽會使用命令的字串形式，後面接著訊息格式（以括弧括住）。</span><span class="sxs-lookup"><span data-stu-id="672cf-120">When commands are discussed, this overview uses the string form of the command followed by the message form in parentheses.</span></span>

 

 
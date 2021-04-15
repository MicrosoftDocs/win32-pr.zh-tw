---
title: 命令訊息
description: 命令訊息
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- MCI 命令訊息，關於
- MCI 命令訊息，語法
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507867"
---
# <a name="command-messages"></a><span data-ttu-id="1f828-106">命令訊息</span><span class="sxs-lookup"><span data-stu-id="1f828-106">Command Messages</span></span>

<span data-ttu-id="1f828-107">命令訊息介面是設計來供需要 C 語言介面來控制多媒體裝置的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="1f828-107">The command-message interface is designed to be used by applications requiring a C-language interface to control multimedia devices.</span></span> <span data-ttu-id="1f828-108">它會使用訊息傳遞範例來與 MCI 裝置通訊。</span><span class="sxs-lookup"><span data-stu-id="1f828-108">It uses a message-passing paradigm to communicate with MCI devices.</span></span> <span data-ttu-id="1f828-109">您可以使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式來傳送命令。</span><span class="sxs-lookup"><span data-stu-id="1f828-109">You can send a command by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="1f828-110">如果成功， **mciSendCommand** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="1f828-110">The **mciSendCommand** function returns zero if successful.</span></span> <span data-ttu-id="1f828-111">如果函式失敗，則傳回值的低序位文字會包含錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1f828-111">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="1f828-112">您可以將此錯誤碼傳遞至 [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) 函式，以取得錯誤的文字描述。</span><span class="sxs-lookup"><span data-stu-id="1f828-112">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-messages"></a><span data-ttu-id="1f828-113">命令訊息的語法</span><span class="sxs-lookup"><span data-stu-id="1f828-113">Syntax of Command Messages</span></span>

<span data-ttu-id="1f828-114">MCI 命令訊息是由下列元素所組成：</span><span class="sxs-lookup"><span data-stu-id="1f828-114">MCI command messages consist of the following elements:</span></span>

-   <span data-ttu-id="1f828-115">常數訊息值</span><span class="sxs-lookup"><span data-stu-id="1f828-115">A constant message value</span></span>
-   <span data-ttu-id="1f828-116">包含命令參數的結構</span><span class="sxs-lookup"><span data-stu-id="1f828-116">A structure containing parameters for the command</span></span>
-   <span data-ttu-id="1f828-117">一組旗標，指定命令的選項以及驗證參數區塊中的欄位</span><span class="sxs-lookup"><span data-stu-id="1f828-117">A set of flags specifying options for the command and validating fields in the parameter block</span></span>

<span data-ttu-id="1f828-118">下列範例會使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式，將 [**MCI \_ PLAY**](mci-play.md) 命令傳送到裝置識別碼所識別的裝置。</span><span class="sxs-lookup"><span data-stu-id="1f828-118">The following example uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send the [**MCI\_ PLAY**](mci-play.md) command to the device identified by a device identifier.</span></span>


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



<span data-ttu-id="1f828-119">使用 [**MCI \_ OPEN**](mci-open.md) 命令開啟裝置時，會抓取第一個參數所提供的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f828-119">The device identifier given in the first parameter is retrieved when the device is opened using the [**MCI\_ OPEN**](mci-open.md) command.</span></span> <span data-ttu-id="1f828-120">最後一個參數是 [**MCI \_ PLAY \_ PARMS**](mci-play-parms.md) 結構的位址，其中可能包含開始及結束播放位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1f828-120">The last parameter is the address of an [**MCI\_ PLAY\_ PARMS**](mci-play-parms.md) structure, which might contain information about where to begin and end playback.</span></span> <span data-ttu-id="1f828-121">許多 MCI 命令訊息都使用結構來包含這種類型的參數。</span><span class="sxs-lookup"><span data-stu-id="1f828-121">Many MCI command messages use a structure to contain parameters of this kind.</span></span> <span data-ttu-id="1f828-122">當作業完成時，每個結構的第一個成員會識別接收 [**MM \_ MCINOTIFY**](mm-mcinotify.md) 訊息的視窗。</span><span class="sxs-lookup"><span data-stu-id="1f828-122">The first member of each of these structures identifies the window that receives an [**MM\_ MCINOTIFY**](mm-mcinotify.md) message when the operation finishes.</span></span>

 

 
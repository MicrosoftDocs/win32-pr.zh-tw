---
title: 命令字串
description: 命令字串
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- MCI 命令字串，關於
- MCI 命令字串，語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104374985"
---
# <a name="command-strings"></a><span data-ttu-id="85da6-105">命令字串</span><span class="sxs-lookup"><span data-stu-id="85da6-105">Command Strings</span></span>

<span data-ttu-id="85da6-106">若要傳送字串命令至 MCI 裝置，請使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式，其中包含字串命令的參數和任何傳回信息的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="85da6-106">To send a string command to an MCI device, use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, which includes parameters for the string command and a buffer for any returned information.</span></span>

<span data-ttu-id="85da6-107">如果成功， **mciSendString** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="85da6-107">The **mciSendString** function returns zero if successful.</span></span> <span data-ttu-id="85da6-108">如果函式失敗，則傳回值的低序位文字會包含錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="85da6-108">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="85da6-109">您可以將此錯誤碼傳遞至 [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) 函式，以取得錯誤的文字描述。</span><span class="sxs-lookup"><span data-stu-id="85da6-109">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-strings"></a><span data-ttu-id="85da6-110">命令字串的語法</span><span class="sxs-lookup"><span data-stu-id="85da6-110">Syntax of Command Strings</span></span>

<span data-ttu-id="85da6-111">MCI 命令字串使用一致的動詞物件修飾詞語法。</span><span class="sxs-lookup"><span data-stu-id="85da6-111">MCI command strings use a consistent verb-object-modifier syntax.</span></span> <span data-ttu-id="85da6-112">每個命令字串都包含一個命令、一個裝置識別碼和一個命令引數。</span><span class="sxs-lookup"><span data-stu-id="85da6-112">Each command string includes a command, a device identifier, and command arguments.</span></span> <span data-ttu-id="85da6-113">某些命令的引數是選擇性的，有些則是必要的。</span><span class="sxs-lookup"><span data-stu-id="85da6-113">Arguments are optional for some commands and required for others.</span></span>

<span data-ttu-id="85da6-114">命令字串的格式如下：</span><span class="sxs-lookup"><span data-stu-id="85da6-114">A command string has the following form:</span></span>

<span data-ttu-id="85da6-115">*命令裝置 \_ 識別碼引數*</span><span class="sxs-lookup"><span data-stu-id="85da6-115">*command device\_id arguments*</span></span>

<span data-ttu-id="85da6-116">這些元件包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="85da6-116">These components contain the following information:</span></span>

-   <span data-ttu-id="85da6-117">此 *命令* 會指定 MCI 命令，例如 [ [**開啟**](open.md)]、[ [**關閉**](close.md)] 或 [ [**播放**](play.md)]。</span><span class="sxs-lookup"><span data-stu-id="85da6-117">The *command* specifies an MCI command, such as [**open**](open.md), [**close**](close.md), or [**play**](play.md).</span></span>
-   <span data-ttu-id="85da6-118">*裝置 \_ 識別碼* 可識別 MCI 驅動程式的實例。</span><span class="sxs-lookup"><span data-stu-id="85da6-118">The *device\_id* identifies an instance of an MCI driver.</span></span> <span data-ttu-id="85da6-119">裝置 *\_ 識別碼* 會在裝置開啟時建立。</span><span class="sxs-lookup"><span data-stu-id="85da6-119">The *device\_id* is created when the device is opened.</span></span>
-   <span data-ttu-id="85da6-120">*引數* 會指定命令所使用的旗標和變數。</span><span class="sxs-lookup"><span data-stu-id="85da6-120">The *arguments* specify the flags and variables used by the command.</span></span> <span data-ttu-id="85da6-121">旗標是使用 MCI 命令辨識的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="85da6-121">Flags are keywords recognized with the MCI command.</span></span> <span data-ttu-id="85da6-122">變數是適用于 MCI 命令或旗標的數位或字串。</span><span class="sxs-lookup"><span data-stu-id="85da6-122">Variables are numbers or strings that apply to the MCI command or flag.</span></span>

    <span data-ttu-id="85da6-123">例如， **play** 命令會使用引數「from *position* 」和「to *position* 」來表示要開始和結束播放的位置。</span><span class="sxs-lookup"><span data-stu-id="85da6-123">For example, the **play** command uses the arguments "from *position* " and "to *position* " to indicate the positions at which to start and end play.</span></span> <span data-ttu-id="85da6-124">您可以依任何順序列出與命令搭配使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="85da6-124">You can list the flags used with a command in any order.</span></span> <span data-ttu-id="85da6-125">當您使用具有與其相關聯之變數的旗標時，您必須提供變數的值。</span><span class="sxs-lookup"><span data-stu-id="85da6-125">When you use a flag that has a variable associated with it, you must supply a value for the variable.</span></span>

    <span data-ttu-id="85da6-126">未指定的 (和選擇性) 命令引數採用預設值。</span><span class="sxs-lookup"><span data-stu-id="85da6-126">Unspecified (and optional) command arguments assume a default value.</span></span>

<span data-ttu-id="85da6-127">下列範例函式會傳送具有 "from" 和 "to" 旗標的 [**play**](play.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="85da6-127">The following example function sends the [**play**](play.md) command with the "from" and "to" flags.</span></span>


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a><span data-ttu-id="85da6-128">命令變數的資料類型</span><span class="sxs-lookup"><span data-stu-id="85da6-128">Data Types for Command Variables</span></span>

<span data-ttu-id="85da6-129">您可以針對命令字串中的變數使用下列資料類型。</span><span class="sxs-lookup"><span data-stu-id="85da6-129">You can use the following data types for the variables in a command string.</span></span>



| <span data-ttu-id="85da6-130">**Data type**</span><span class="sxs-lookup"><span data-stu-id="85da6-130">**Data type**</span></span>        | <span data-ttu-id="85da6-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="85da6-131">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85da6-132">字串</span><span class="sxs-lookup"><span data-stu-id="85da6-132">Strings</span></span>              | <span data-ttu-id="85da6-133">字串資料類型會以開頭和尾端的空白字元和引號分隔。</span><span class="sxs-lookup"><span data-stu-id="85da6-133">String data types are delimited by leading and trailing white spaces and quotation marks.</span></span> <span data-ttu-id="85da6-134">MCI 從字串移除單引號。</span><span class="sxs-lookup"><span data-stu-id="85da6-134">MCI removes single quotation marks from a string.</span></span> <span data-ttu-id="85da6-135">若要在字串中放入引號，請使用一組您想要內嵌引號的雙引號。</span><span class="sxs-lookup"><span data-stu-id="85da6-135">To put a quotation mark in a string, use a set of two quotation marks where you want to embed your quotation mark.</span></span> <span data-ttu-id="85da6-136">若要使用空字串，請使用以開頭和尾端空格分隔的兩個引號。</span><span class="sxs-lookup"><span data-stu-id="85da6-136">To use an empty string, use two quotation marks delimited by leading and trailing white spaces.</span></span> |
| <span data-ttu-id="85da6-137">帶正負號的長整數</span><span class="sxs-lookup"><span data-stu-id="85da6-137">Signed long integers</span></span> | <span data-ttu-id="85da6-138">帶正負號的長整數資料類型會以開頭和尾端空格分隔。</span><span class="sxs-lookup"><span data-stu-id="85da6-138">Signed long integer data types are delimited by leading and trailing white spaces.</span></span> <span data-ttu-id="85da6-139">除非另有指定，否則整數可以是正數或負數。</span><span class="sxs-lookup"><span data-stu-id="85da6-139">Unless otherwise specified, integers can be positive or negative.</span></span> <span data-ttu-id="85da6-140">如果您使用負整數，則不應以空格分隔減號和第一個數位。</span><span class="sxs-lookup"><span data-stu-id="85da6-140">If you use negative integers, you should not separate the minus sign and the first digit with a space.</span></span>                                                                                                    |
| <span data-ttu-id="85da6-141">矩形</span><span class="sxs-lookup"><span data-stu-id="85da6-141">Rectangles</span></span>           | <span data-ttu-id="85da6-142">矩形資料類型是四個帶正負號短值的排序清單。</span><span class="sxs-lookup"><span data-stu-id="85da6-142">Rectangle data types are an ordered list of four signed short values.</span></span> <span data-ttu-id="85da6-143">空白字元會分隔此資料類型，並分隔清單中的每個整數。</span><span class="sxs-lookup"><span data-stu-id="85da6-143">White space delimits this data type and separates each integer in the list.</span></span>                                                                                                                                                                                                              |



 

 

 
---
title: MCI 函數宏和訊息
description: MCI 函數宏和訊息
ms.assetid: 7cedc46f-f67b-4b1a-b1e0-7ac32c250132
keywords:
- MCI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade9ac3ea5c2a3c74f94bab899305cdae7ec51c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682281"
---
# <a name="mci-functions-macros-and-messages"></a><span data-ttu-id="19c0d-104">MCI 函數宏和訊息</span><span class="sxs-lookup"><span data-stu-id="19c0d-104">MCI Functions Macros and Messages</span></span>

<span data-ttu-id="19c0d-105">大部分的 MCI 應用程式會使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 和 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數數十次。</span><span class="sxs-lookup"><span data-stu-id="19c0d-105">Most MCI applications use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) and [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) functions dozens of times.</span></span> <span data-ttu-id="19c0d-106">MCI 提供一些其他有用的功能，讓您的應用程式不會經常使用。</span><span class="sxs-lookup"><span data-stu-id="19c0d-106">MCI provides some other useful functions that your application will use less frequently.</span></span>

<span data-ttu-id="19c0d-107">大部分 MCI 命令所需的裝置識別碼，通常是在 [**open**](open.md) ([**mci \_ open**](mci-open.md)) 命令的呼叫中取出。</span><span class="sxs-lookup"><span data-stu-id="19c0d-107">The device identifier required by most MCI commands is typically retrieved in a call to the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span> <span data-ttu-id="19c0d-108">如果您需要裝置識別碼，但不想要開啟裝置，例如，如果您想要查詢裝置的功能再採取任何其他動作，您可以呼叫 [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) 函式。</span><span class="sxs-lookup"><span data-stu-id="19c0d-108">If you need a device identifier but do not want to open the device — for example, if you want to query the capabilities of the device before taking any other action — you can call the [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) function.</span></span>

<span data-ttu-id="19c0d-109">[**MciGetCreatorTask**](/previous-versions//dd757155(v=vs.85))函式可讓您的應用程式使用裝置識別碼，來取得建立該識別碼之工作的控制碼。</span><span class="sxs-lookup"><span data-stu-id="19c0d-109">The [**mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85)) function allows your application to use a device identifier to retrieve a handle to the task that created that identifier.</span></span>

<span data-ttu-id="19c0d-110">您可以使用 [**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85)) 和 [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85)) 函式來指派和取出與 "wait" (MCI wait) 旗標相關聯的回呼函式位址 \_ 。</span><span class="sxs-lookup"><span data-stu-id="19c0d-110">You can use the [**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85)) and [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85)) functions to assign and retrieve the address of the callback function associated with the "wait" (MCI\_WAIT) flag.</span></span>

<span data-ttu-id="19c0d-111">[**MciGetErrorString**](/previous-versions//dd757158(v=vs.85))函式會捕獲描述 MCI 錯誤值的字串。</span><span class="sxs-lookup"><span data-stu-id="19c0d-111">The [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function retrieves a string that describes an MCI error value.</span></span> <span data-ttu-id="19c0d-112">MCI 傳回的每個字串（不論是資料還是錯誤描述）最多為128個字元。</span><span class="sxs-lookup"><span data-stu-id="19c0d-112">Each string that MCI returns, whether data or an error description, is a maximum of 128 characters.</span></span> <span data-ttu-id="19c0d-113">小於128個字元的對話方塊欄位將截斷 MCI 傳回的較長字串。</span><span class="sxs-lookup"><span data-stu-id="19c0d-113">Dialog box fields that are smaller than 128 characters will truncate the longer strings returned by MCI.</span></span> <span data-ttu-id="19c0d-114">如需這些字串的詳細資訊，請參閱 [MCIERR 傳回值](mcierr-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="19c0d-114">For more information about these strings, see [MCIERR Return Values](mcierr-return-values.md).</span></span>

<span data-ttu-id="19c0d-115">MCI 宏是您可用來建立和分解指定時間格式之值的工具。</span><span class="sxs-lookup"><span data-stu-id="19c0d-115">The MCI macros are tools you can use to create and disassemble values that specify time formats.</span></span> <span data-ttu-id="19c0d-116">這些時間格式用於許多 MCI 命令中。</span><span class="sxs-lookup"><span data-stu-id="19c0d-116">These time formats are used in many MCI commands.</span></span> <span data-ttu-id="19c0d-117">宏所處理的格式為小時/分鐘/秒 (HMS) 、分鐘/秒/畫面格 (MSF) ，以及追蹤/分/秒/畫面格 (TMSF) 。</span><span class="sxs-lookup"><span data-stu-id="19c0d-117">The formats acted on by the macros are hours/minutes/seconds (HMS), minutes/seconds/frames (MSF), and tracks/minutes/seconds/frames (TMSF).</span></span> <span data-ttu-id="19c0d-118">下表列出宏及其描述。</span><span class="sxs-lookup"><span data-stu-id="19c0d-118">The following table lists the macros and their descriptions.</span></span>



| <span data-ttu-id="19c0d-119">巨集</span><span class="sxs-lookup"><span data-stu-id="19c0d-119">Macro</span></span>                                        | <span data-ttu-id="19c0d-120">Description</span><span class="sxs-lookup"><span data-stu-id="19c0d-120">Description</span></span>                                        |
|----------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="19c0d-121">**MCI \_ HMS \_ HOUR**</span><span class="sxs-lookup"><span data-stu-id="19c0d-121">**MCI\_HMS\_HOUR**</span></span>](mci-hms-hour.md)       | <span data-ttu-id="19c0d-122">從 HMS 值抓取小時元件。</span><span class="sxs-lookup"><span data-stu-id="19c0d-122">Retrieves the hours component from an HMS value.</span></span>   |
| [<span data-ttu-id="19c0d-123">**MCI \_ HMS \_ 分鐘**</span><span class="sxs-lookup"><span data-stu-id="19c0d-123">**MCI\_HMS\_MINUTE**</span></span>](mci-hms-minute.md)   | <span data-ttu-id="19c0d-124">從 HMS 值抓取分鐘元件。</span><span class="sxs-lookup"><span data-stu-id="19c0d-124">Retrieves the minutes component from an HMS value.</span></span> |
| [<span data-ttu-id="19c0d-125">**MCI \_ HMS \_ SECOND**</span><span class="sxs-lookup"><span data-stu-id="19c0d-125">**MCI\_HMS\_SECOND**</span></span>](mci-hms-second.md)   | <span data-ttu-id="19c0d-126">從 HMS 值抓取秒鐘元件。</span><span class="sxs-lookup"><span data-stu-id="19c0d-126">Retrieves the seconds component from an HMS value.</span></span> |
| [<span data-ttu-id="19c0d-127">**MCI \_ 製作 \_ HMS**</span><span class="sxs-lookup"><span data-stu-id="19c0d-127">**MCI\_MAKE\_HMS**</span></span>](mci-make-hms.md)       | <span data-ttu-id="19c0d-128">建立 HMS 值。</span><span class="sxs-lookup"><span data-stu-id="19c0d-128">Creates an HMS value.</span></span>                              |
| [<span data-ttu-id="19c0d-129">**MCI \_ 讓 \_ MSF**</span><span class="sxs-lookup"><span data-stu-id="19c0d-129">**MCI\_MAKE\_MSF**</span></span>](mci-make-msf.md)       | <span data-ttu-id="19c0d-130">建立 MSF 值。</span><span class="sxs-lookup"><span data-stu-id="19c0d-130">Creates an MSF value.</span></span>                              |
| [<span data-ttu-id="19c0d-131">**MCI \_ 製作 \_ TMSF**</span><span class="sxs-lookup"><span data-stu-id="19c0d-131">**MCI\_MAKE\_TMSF**</span></span>](mci-make-tmsf.md)     | <span data-ttu-id="19c0d-132">建立 TMSF 值。</span><span class="sxs-lookup"><span data-stu-id="19c0d-132">Creates a TMSF value.</span></span>                              |
| <span data-ttu-id="19c0d-133">[**MCI \_ MSF \_ 框架**](/previous-versions//dd743438(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19c0d-133">[**MCI\_MSF\_FRAME**](/previous-versions//dd743438(v=vs.85))</span></span>     | <span data-ttu-id="19c0d-134">從 MSF 值抓取畫面格元件。</span><span class="sxs-lookup"><span data-stu-id="19c0d-134">Retrieves the frames component from an MSF value.</span></span>  |
| [<span data-ttu-id="19c0d-135">**MCI \_ MSF \_ 分鐘**</span><span class="sxs-lookup"><span data-stu-id="19c0d-135">**MCI\_MSF\_MINUTE**</span></span>](mci-msf-minute.md)   | <span data-ttu-id="19c0d-136">從 MSF 值抓取分鐘元件。</span><span class="sxs-lookup"><span data-stu-id="19c0d-136">Retrieves the minutes component from an MSF value.</span></span> |
| [<span data-ttu-id="19c0d-137">**MCI \_ MSF \_ SECOND**</span><span class="sxs-lookup"><span data-stu-id="19c0d-137">**MCI\_MSF\_SECOND**</span></span>](mci-msf-second.md)   | <span data-ttu-id="19c0d-138">從 MSF 值抓取秒鐘元件。</span><span class="sxs-lookup"><span data-stu-id="19c0d-138">Retrieves the seconds component from an MSF value.</span></span> |
| [<span data-ttu-id="19c0d-139">**MCI \_ TMSF \_ 框架**</span><span class="sxs-lookup"><span data-stu-id="19c0d-139">**MCI\_TMSF\_FRAME**</span></span>](mci-tmsf-frame.md)   | <span data-ttu-id="19c0d-140">從 TMSF 值抓取畫面格元件。</span><span class="sxs-lookup"><span data-stu-id="19c0d-140">Retrieves the frames component from a TMSF value.</span></span>  |
| [<span data-ttu-id="19c0d-141">**MCI \_ TMSF \_ 分鐘**</span><span class="sxs-lookup"><span data-stu-id="19c0d-141">**MCI\_TMSF\_MINUTE**</span></span>](mci-tmsf-minute.md) | <span data-ttu-id="19c0d-142">從 TMSF 值抓取分鐘元件。</span><span class="sxs-lookup"><span data-stu-id="19c0d-142">Retrieves the minutes component from a TMSF value.</span></span> |
| [<span data-ttu-id="19c0d-143">**MCI \_ TMSF \_ SECOND**</span><span class="sxs-lookup"><span data-stu-id="19c0d-143">**MCI\_TMSF\_SECOND**</span></span>](mci-tmsf-second.md) | <span data-ttu-id="19c0d-144">從 TMSF 值抓取秒鐘元件。</span><span class="sxs-lookup"><span data-stu-id="19c0d-144">Retrieves the seconds component from a TMSF value.</span></span> |
| [<span data-ttu-id="19c0d-145">**MCI \_ TMSF \_ TRACK**</span><span class="sxs-lookup"><span data-stu-id="19c0d-145">**MCI\_TMSF\_TRACK**</span></span>](mci-tmsf-track.md)   | <span data-ttu-id="19c0d-146">從 TMSF 值抓取追蹤元件。</span><span class="sxs-lookup"><span data-stu-id="19c0d-146">Retrieves the tracks component from a TMSF value.</span></span>  |



 

<span data-ttu-id="19c0d-147">MCI 也提供兩個訊息： [**MM \_ MCINOTIFY**](mm-mcinotify.md) 和 [**mm \_ MCISIGNAL**](mm-mcisignal.md)。</span><span class="sxs-lookup"><span data-stu-id="19c0d-147">MCI also provides two messages: [**MM\_MCINOTIFY**](mm-mcinotify.md) and [**MM\_MCISIGNAL**](mm-mcisignal.md).</span></span> <span data-ttu-id="19c0d-148">\_只要命令指定「通知」 (mci 通知) 旗標，MM MCINOTIFY 訊息就會通知應用程式是否有 mci 命令的結果 \_ 。</span><span class="sxs-lookup"><span data-stu-id="19c0d-148">The MM\_MCINOTIFY message notifies an application of the outcome of an MCI command whenever that command specifies the "notify" (MCI\_NOTIFY) flag.</span></span> <span data-ttu-id="19c0d-149">MM \_ MCISIGNAL 訊息是數位視訊裝置的特定訊息; 當達到指定的位置時，就會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="19c0d-149">The MM\_MCISIGNAL message is specific to digital-video devices; it notifies the application when a specified position is reached.</span></span>

 

 
---
description: 命令
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: '命令 (WPD API) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191286"
---
# <a name="commands-wpd-api"></a><span data-ttu-id="a7a2b-103">命令 (WPD API) </span><span class="sxs-lookup"><span data-stu-id="a7a2b-103">Commands (WPD API)</span></span>

<span data-ttu-id="a7a2b-104">用戶端應用程式和驅動程式會藉由從用戶端 (透過 User-Mode 驅動程式架構) 透過 Windows 可攜式裝置 API) 傳送至驅動程式 (的命令進行通訊。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-104">The client application and the driver communicate by means of commands that are sent from the client (via the Windows Portable Device API) to the driver (via the User-Mode Driver Framework).</span></span> <span data-ttu-id="a7a2b-105">命令不一定會包含參數，且不一定會傳回結果。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-105">A command may or may not include a parameter, and may or may not return a result.</span></span> <span data-ttu-id="a7a2b-106">用戶端可以呼叫 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) 方法或 **IPortableDeviceService： SendCommand** 方法，或藉由呼叫用戶端介面的任何方法，以明確地傳送命令。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-106">A client can send a command explicitly, by calling either the [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) method or the **IPortableDeviceService:SendCommand** method, or implicitly, by calling any of the methods of the client interfaces.</span></span> <span data-ttu-id="a7a2b-107">只有一些命令可以明確地傳送;這些會在命令的檔中注明。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-107">A few commands can only be sent explicitly; these are noted in the command's documentation.</span></span> <span data-ttu-id="a7a2b-108">命令參考頁面描述命令的用途，以及它預期要接收的參數，以及預期會傳回的參數。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-108">The command reference pages describe the purpose of a command, as well as what parameters it expects to receive, and what parameters it is expected to return.</span></span>

<span data-ttu-id="a7a2b-109">命令是由 **PROPERTYKEY** 結構所識別。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-109">A command is identified by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="a7a2b-110">這是由兩個部分所組成： GUID 部分 (*fmtid* 成員) 和 (*pid* 成員) 的 DWORD 部分。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-110">This is made up of two parts: a GUID part (the *fmtid* member) and a DWORD part (the *pid* member).</span></span> <span data-ttu-id="a7a2b-111">GUID 部分可用來指出命令所屬類別 (相關命令屬於相同的類別，因此將會有相同的 *fmtid*) 。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-111">The GUID part is used to indicate the category the command belongs to (related commands belong to the same category, and therefore will have the same *fmtid*).</span></span> <span data-ttu-id="a7a2b-112">DWORD 部分表示命令識別碼，用來區別命令類別中的個別命令 (相同類別中命令的 *pid* 值會) 不同。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-112">The DWORD part indicates the command ID, and is used to distinguish the individual commands within a command category (the *pid* values for commands in the same category will be different).</span></span>

<span data-ttu-id="a7a2b-113">下表列出 Windows 可攜式裝置所定義命令的類別。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-113">The following table lists the categories of commands that Windows Portable Devices defines.</span></span> <span data-ttu-id="a7a2b-114">裝置製造商可以藉由建立自己的命令類別和命令識別碼，來定義自己的命令。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-114">Device manufacturers can define their own commands by creating their own command categories and command IDs.</span></span> <span data-ttu-id="a7a2b-115">不過，製造商不應將命令新增至下列類別，因為這些是由 Microsoft 所保留的類別。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-115">However, a manufacturer should not add commands to the categories listed below, since these are reserved by Microsoft.</span></span>

<span data-ttu-id="a7a2b-116">**命令類別目錄**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-116">**Command Categories**</span></span>



| <span data-ttu-id="a7a2b-117">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="a7a2b-117">Command category</span></span>                         | <span data-ttu-id="a7a2b-118">Description</span><span class="sxs-lookup"><span data-stu-id="a7a2b-118">Description</span></span>                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a2b-119">**WPD \_ 類別 \_ 通用**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-119">**WPD\_CATEGORY\_COMMON**</span></span>                | <span data-ttu-id="a7a2b-120">所有物件和裝置通用的命令。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-120">Commands that are common to all objects and devices.</span></span>                                                                                    |
| <span data-ttu-id="a7a2b-121">**WPD \_ 類別 \_ 裝置 \_ 提示**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-121">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>         | <span data-ttu-id="a7a2b-122">用來取得選擇性裝置資訊的命令，可用來改善終端使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-122">Commands that are used to retrieve optional device information that can be used to improve end-user experience.</span></span>                         |
| <span data-ttu-id="a7a2b-123">**WPD \_ 類別 \_ SMS**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-123">**WPD\_CATEGORY\_SMS**</span></span>                   | <span data-ttu-id="a7a2b-124">用於支援短訊息服務之裝置的命令 (SMS) 功能，這通常會在行動電話上公開。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-124">Commands that are used for devices that support short message service (SMS) functionality, which is typically exposed on mobile phones.</span></span> |
| <span data-ttu-id="a7a2b-125">**WPD \_ 類別 \_ 仍為 \_ 影像 \_ 捕捉**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-125">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span> | <span data-ttu-id="a7a2b-126">用於支援仍為影像捕捉之裝置的命令。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-126">Commands that are used for devices that support still image capture.</span></span>                                                                    |
| <span data-ttu-id="a7a2b-127">**WPD \_ 類別 \_ 儲存體**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-127">**WPD\_CATEGORY\_STORAGE**</span></span>               | <span data-ttu-id="a7a2b-128">用於儲存功能物件的命令。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-128">Commands that are used for storage functional objects.</span></span>                                                                                  |



 

<span data-ttu-id="a7a2b-129">下表中會提供針對每個類型定義的特定命令，並依命令類型進行組織。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-129">The specific commands that are defined for each of these types are given in the following tables, organized by command type.</span></span>

<span data-ttu-id="a7a2b-130">**WPD \_ 類別 \_ 一般分類**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-130">**WPD\_CATEGORY\_COMMON Category**</span></span>



| <span data-ttu-id="a7a2b-131">命令</span><span class="sxs-lookup"><span data-stu-id="a7a2b-131">Command</span></span>                                                                                | <span data-ttu-id="a7a2b-132">描述</span><span class="sxs-lookup"><span data-stu-id="a7a2b-132">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="a7a2b-133">**WPD \_ 命令 \_ 一般 \_ 重設 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-133">**WPD\_COMMAND\_COMMON\_RESET\_DEVICE**</span></span>](wpd-command-common-reset-device-command.md) | <span data-ttu-id="a7a2b-134">重設裝置。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-134">Resets the device.</span></span> |



 

<span data-ttu-id="a7a2b-135">**WPD \_ 類別 \_ 裝置 \_ 提示分類**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-135">**WPD\_CATEGORY\_DEVICE\_HINTS Category**</span></span>



| <span data-ttu-id="a7a2b-136">命令</span><span class="sxs-lookup"><span data-stu-id="a7a2b-136">Command</span></span>                                                                                                              | <span data-ttu-id="a7a2b-137">描述</span><span class="sxs-lookup"><span data-stu-id="a7a2b-137">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="a7a2b-138">**WPD \_ 命令 \_ 裝置 \_ 提示 \_ 取得 \_ 內容 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-138">**WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION**</span></span>](wpd-command-device-hints-get-content-location-command.md) | <span data-ttu-id="a7a2b-139">抓取可保存指定類型物件之資料夾的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-139">Retrieves the object IDs of folders that can hold an object of a specified type.</span></span> |



 

<span data-ttu-id="a7a2b-140">**WPD \_ 類別 \_ 儲存體類別**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-140">**WPD\_CATEGORY\_STORAGE Category**</span></span>



| <span data-ttu-id="a7a2b-141">命令</span><span class="sxs-lookup"><span data-stu-id="a7a2b-141">Command</span></span>                                                                     | <span data-ttu-id="a7a2b-142">描述</span><span class="sxs-lookup"><span data-stu-id="a7a2b-142">Description</span></span>                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="a7a2b-143">**WPD \_ 命令 \_ 儲存體 \_ 退出**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-143">**WPD\_COMMAND\_STORAGE\_EJECT**</span></span>](wpd-command-storage-eject-command.md)   | <span data-ttu-id="a7a2b-144">彈出可由驅動程式從遠端彈出的儲存媒體。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-144">Ejects a storage medium that can be ejected remotely by the driver.</span></span> |
| [<span data-ttu-id="a7a2b-145">**WPD \_ 命令 \_ 單元 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-145">**WPD\_COMMAND\_STORAGE\_FORMAT**</span></span>](wpd-command-storage-format-command.md) | <span data-ttu-id="a7a2b-146">將裝置上的儲存功能物件格式化。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-146">Formats a storage functional object on the device.</span></span>                  |



 

<span data-ttu-id="a7a2b-147">**WPD \_ 類別目錄 \_ SMS 類別目錄**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-147">**WPD\_CATEGORY\_SMS Category**</span></span>



| <span data-ttu-id="a7a2b-148">命令</span><span class="sxs-lookup"><span data-stu-id="a7a2b-148">Command</span></span>                                                         | <span data-ttu-id="a7a2b-149">描述</span><span class="sxs-lookup"><span data-stu-id="a7a2b-149">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="a7a2b-150">**WPD \_ 命令 \_ SMS \_ SEND**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-150">**WPD\_COMMAND\_SMS\_SEND**</span></span>](wpd-command-sms-send-command.md) | <span data-ttu-id="a7a2b-151">起始 sms 功能物件傳送 SMS 訊息。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-151">Initiates the sending of an SMS message by an SMS functional object.</span></span> |



 

<span data-ttu-id="a7a2b-152">**WPD \_ 類別 \_ 仍為 \_ 影像 \_ 捕獲類別**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-152">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE Category**</span></span>



| <span data-ttu-id="a7a2b-153">命令</span><span class="sxs-lookup"><span data-stu-id="a7a2b-153">Command</span></span>                                                                                                   | <span data-ttu-id="a7a2b-154">描述</span><span class="sxs-lookup"><span data-stu-id="a7a2b-154">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="a7a2b-155">**WPD \_ 命令 \_ 仍為 \_ 映射 \_ 捕獲 \_ 起始**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-155">**WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE**</span></span>](wpd-command-still-image-capture-initiate-command.md) | <span data-ttu-id="a7a2b-156">使用靜止影像功能物件起始靜止的影像捕捉。</span><span class="sxs-lookup"><span data-stu-id="a7a2b-156">Initiates a still image capture by a still image functional object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a7a2b-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7a2b-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7a2b-158">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="a7a2b-158">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




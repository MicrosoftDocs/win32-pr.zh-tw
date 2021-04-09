---
title: 命令快捷方式和變化
description: 命令快捷方式和變化
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674552"
---
# <a name="command-shortcuts-and-variations"></a><span data-ttu-id="c1c0b-103">命令快捷方式和變化</span><span class="sxs-lookup"><span data-stu-id="c1c0b-103">Command Shortcuts and Variations</span></span>

<span data-ttu-id="c1c0b-104">使用 MCI 命令時，您可以使用數個快捷方式。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-104">You can use several shortcuts when working with MCI commands.</span></span> <span data-ttu-id="c1c0b-105">這些快捷方式可讓您使用單一識別碼來參考您的應用程式已開啟的所有裝置，或在未明確發出 [**開啟**](open.md) 的 ([**MCI \_ 開啟**](mci-open.md)) 命令的情況下開啟裝置。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-105">These shortcuts enable you to use a single identifier to refer to all the devices your application has opened, or to open a device without explicitly issuing an [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="c1c0b-106">您可以指定 "all" (MCI \_ 所有 \_ 裝置 \_ 識別碼) 作為任何未傳回信息之命令的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-106">You can specify "all" (MCI\_ALL\_DEVICE\_ID) as a device identifier for any command that does not return information.</span></span> <span data-ttu-id="c1c0b-107">當您指定 "all" 時，MCI 會依序將命令傳送至目前應用程式所開啟的所有裝置。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-107">When you specify "all", MCI sends the command sequentially to all devices opened by the current application.</span></span>

<span data-ttu-id="c1c0b-108">例如， [**close**](close.md) "all" 命令會關閉所有開啟的裝置，而 [**play**](play.md) "all" 命令會開始播放應用程式所開啟的所有裝置。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-108">For example, the [**close**](close.md) "all" command closes all open devices and the [**play**](play.md) "all" command starts playing all devices opened by the application.</span></span> <span data-ttu-id="c1c0b-109">由於 MCI 會依序將命令傳送至 MCI 裝置，因此第一個和最後一個裝置收到命令的間隔會有一段時間。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-109">Because MCI sequentially sends the commands to the MCI devices, there is an interval between when the first and last devices receive the command.</span></span>

<span data-ttu-id="c1c0b-110">使用「全部」是將命令廣播到所有裝置的便利方法，但您不應該依賴它來同步處理裝置;訊息之間的時間可能會有所不同。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-110">Using "all" is a convenient way to broadcast a command to all your devices, but you should not rely on it to synchronize devices; the timing between messages can vary.</span></span>

<span data-ttu-id="c1c0b-111">當您發出命令並指定未開啟的裝置時，MCI 會嘗試在執行命令之前先開啟裝置。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-111">When you issue a command and specify a device that is not open, MCI tries to open the device before implementing the command.</span></span> <span data-ttu-id="c1c0b-112">下列規則適用于自動開啟裝置：</span><span class="sxs-lookup"><span data-stu-id="c1c0b-112">The following rules apply to automatically opening devices:</span></span>

-   <span data-ttu-id="c1c0b-113">自動開啟功能只適用于命令字串介面。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-113">The automatic open feature works only with the command-string interface.</span></span>
-   <span data-ttu-id="c1c0b-114">針對自訂設備磁碟機特定的命令，自動開啟功能會失敗。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-114">The automatic open feature fails for commands that are specific to custom device drivers.</span></span>
-   <span data-ttu-id="c1c0b-115">自動開啟的裝置不會回應使用 "all" 作為裝置名稱的命令。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-115">Automatically opened devices do not respond to commands that use "all" as a device name.</span></span>
-   <span data-ttu-id="c1c0b-116">自動開啟功能不會讓您的應用程式指定「類型」旗標。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-116">The automatic open feature does not let your application specify the "type" flag.</span></span> <span data-ttu-id="c1c0b-117">如果沒有裝置名稱，MCI 會從登錄中的專案決定裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-117">Without the device name, MCI determines the device name from the entries in the registry.</span></span> <span data-ttu-id="c1c0b-118">若要使用特定的裝置，您可以使用 [ [**開啟**](open.md) ] 命令的參考資料中所述的驚嘆號來結合裝置名稱與檔案名。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-118">To use a specific device, you can combine the device name with the filename by using the exclamation point, as described in the reference material for the [**open**](open.md) command.</span></span>

<span data-ttu-id="c1c0b-119">如果應用程式使用自動開啟功能來開啟裝置，應用程式應該檢查每個後續開啟命令的傳回值，以確認裝置仍處於開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-119">If an application uses the automatic open feature to open a device, the application should check the return value of every subsequent open command to verify that the device is still open.</span></span> <span data-ttu-id="c1c0b-120">MCI 也會自動關閉自動開啟的任何裝置。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-120">MCI also automatically closes any device that it automatically opens.</span></span> <span data-ttu-id="c1c0b-121">在下列情況下，MCI 通常會關閉裝置：</span><span class="sxs-lookup"><span data-stu-id="c1c0b-121">MCI typically closes a device in the following situations:</span></span>

-   <span data-ttu-id="c1c0b-122">此命令已完成。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-122">The command is completed.</span></span>
-   <span data-ttu-id="c1c0b-123">您會中止命令。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-123">You abort the command.</span></span>
-   <span data-ttu-id="c1c0b-124">您會在後續命令中要求通知。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-124">You request notification in a subsequent command.</span></span>
-   <span data-ttu-id="c1c0b-125">MCI 偵測到失敗。</span><span class="sxs-lookup"><span data-stu-id="c1c0b-125">MCI detects a failure.</span></span>

 

 





---
title: 裝置存取詞彙
description: 以下是在裝置存取 API 的檔中使用的詞彙。
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374342"
---
# <a name="device-access-glossary"></a><span data-ttu-id="45778-103">裝置存取詞彙</span><span class="sxs-lookup"><span data-stu-id="45778-103">Device Access Glossary</span></span>

<span data-ttu-id="45778-104">以下是在裝置存取 API 的檔中使用的詞彙。</span><span class="sxs-lookup"><span data-stu-id="45778-104">The following are terms used throughout the documentation for the Device Access API.</span></span>

<dl> <dt>

<span data-ttu-id="45778-105">**AppContainer**</span><span class="sxs-lookup"><span data-stu-id="45778-105">**AppContainer**</span></span>
</dt> <dd>

<span data-ttu-id="45778-106">高度受限的執行環境，在此環境中，進程會以精簡的使用者許可權子集來執行。</span><span class="sxs-lookup"><span data-stu-id="45778-106">A highly restricted execution environment in which a process runs with a reduced subset of the user's privileges.</span></span> <span data-ttu-id="45778-107">在 AppContainer 內執行的進程稱為 AppContainer 處理常式。</span><span class="sxs-lookup"><span data-stu-id="45778-107">A process that's running within an AppContainer is called an AppContainer process.</span></span> <span data-ttu-id="45778-108">AppContainer 進程與其他 AppContainer 進程和使用者的設定檔隔離。</span><span class="sxs-lookup"><span data-stu-id="45778-108">An AppContainer process is isolated from other AppContainer processes and from the user's profile.</span></span> <span data-ttu-id="45778-109">它對一小部分的系統資源（例如檔案、裝置、登錄機碼、處理序間通訊 (IPC) /remote 程序呼叫 (RPC) 端點和網路資源）具有有限的存取權。</span><span class="sxs-lookup"><span data-stu-id="45778-109">It has limited access to a very small subset of system resources like files, devices, registry keys, interprocess communication (IPC)/remote procedure call (RPC) endpoints, and network resources.</span></span>

</dd> <dt>

<span data-ttu-id="45778-110">**繫結**</span><span class="sxs-lookup"><span data-stu-id="45778-110">**Binding**</span></span>
</dt> <dd>

<span data-ttu-id="45778-111">將裝置存取物件與特定裝置介面產生關聯。</span><span class="sxs-lookup"><span data-stu-id="45778-111">Associating a device access object with a particular device interface.</span></span> <span data-ttu-id="45778-112">如果系結成功，Windows Store 應用程式就可以使用裝置存取物件作為訊息代理程式來與設備磁碟機進行通訊。</span><span class="sxs-lookup"><span data-stu-id="45778-112">If binding is successful, Windows Store apps can use the device access object as a broker to communicate with the device driver.</span></span>

</dd> <dt>

<span data-ttu-id="45778-113">**Broker**</span><span class="sxs-lookup"><span data-stu-id="45778-113">**Broker**</span></span>
</dt> <dd>

<span data-ttu-id="45778-114">元件，可存取預設不會授與的資源。</span><span class="sxs-lookup"><span data-stu-id="45778-114">A component that provides access to a resource that isn't granted by default.</span></span>

</dd> <dt>

<span data-ttu-id="45778-115">**具特殊許可權的應用程式**</span><span class="sxs-lookup"><span data-stu-id="45778-115">**Privileged App**</span></span>
</dt> <dd>

<span data-ttu-id="45778-116">在特定裝置的中繼資料中識別為與該裝置相關聯的應用程式，讓它可以與設備磁碟機的受限制介面進行通訊。</span><span class="sxs-lookup"><span data-stu-id="45778-116">An app that's identified in a particular device's metadata as associated with that device, so that it can communicate with the device driver's restricted interface.</span></span> <span data-ttu-id="45778-117">這類應用程式的範例可能是專屬的音樂播放應用程式，當競爭者的應用程式無法使用時，其具有與便攜音樂播放機同步的獨佔許可權。</span><span class="sxs-lookup"><span data-stu-id="45778-117">An example of such an app might be a proprietary music playback app that has exclusive permission to sync with a portable music player, when apps from competitors can't.</span></span> <span data-ttu-id="45778-118">如需有關如何設定裝置的中繼資料，或如何將驅動程式限制在特殊許可權應用程式的詳細資訊，請參閱 [適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)。</span><span class="sxs-lookup"><span data-stu-id="45778-118">For more information about how to set a device's metadata or how to restrict a driver to privileged apps, see [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span></span>

</dd> </dl>

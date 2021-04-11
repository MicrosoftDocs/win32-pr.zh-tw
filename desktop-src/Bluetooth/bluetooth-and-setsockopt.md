---
title: 藍牙和 setsockopt
description: 藍牙使用 setsockopt 函式來設定與伺服器通道或連接相關聯的各種參數。
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- 藍牙和 setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315343"
---
# <a name="bluetooth-and-setsockopt"></a><span data-ttu-id="0928e-106">藍牙和 setsockopt</span><span class="sxs-lookup"><span data-stu-id="0928e-106">Bluetooth and setsockopt</span></span>

<span data-ttu-id="0928e-107">藍牙使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式來設定與伺服器通道或連接相關聯的各種參數。</span><span class="sxs-lookup"><span data-stu-id="0928e-107">Bluetooth uses the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="0928e-108">使用 **setsockopt** 搭配藍牙有下列需求：</span><span class="sxs-lookup"><span data-stu-id="0928e-108">Use of **setsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="0928e-109">[**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)的 *s* 參數必須是有效的藍牙通訊端。</span><span class="sxs-lookup"><span data-stu-id="0928e-109">The *s* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="0928e-110">[**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)的 *level* 參數必須是 SOL \_ RFCOMM。</span><span class="sxs-lookup"><span data-stu-id="0928e-110">The *level* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="0928e-111">如需可用藍牙通訊端選項的清單，請參閱 [藍牙和通訊端選項](bluetooth-and-socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="0928e-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0928e-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="0928e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0928e-113">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="0928e-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="0928e-114">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="0928e-114">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
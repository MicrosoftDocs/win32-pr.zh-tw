---
title: 修改裝置重新導向預設值
description: 因為遠端桌面閘道伺服器在將用戶端連線傳遞到遠端桌面工作階段主機伺服器之前，嘗試強制執行安全的裝置重新導向原則，所以在某些情況下，您可能需要停用此預設值。
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840176"
---
# <a name="modify-device-redirection-default"></a><span data-ttu-id="4ee27-103">修改裝置重新導向預設值</span><span class="sxs-lookup"><span data-stu-id="4ee27-103">Modify Device Redirection Default</span></span>

<span data-ttu-id="4ee27-104">因為遠端桌面閘道伺服器在將用戶端連線傳遞到遠端桌面工作階段主機伺服器之前，嘗試強制執行安全的裝置重新導向原則，所以在某些情況下，您可能需要停用此預設值。</span><span class="sxs-lookup"><span data-stu-id="4ee27-104">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

<span data-ttu-id="4ee27-105">在 Windows Server 2008 R2 和更新版本上，遠端桌面閘道伺服器預設會嘗試強制執行安全的裝置重新導向原則，然後才將用戶端連線傳遞到遠端桌面工作階段主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="4ee27-105">On Windows Server 2008 R2 and later, Remote Desktop Gateway servers will by default attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server.</span></span> <span data-ttu-id="4ee27-106">不過，某些伺服器並不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="4ee27-106">However, this feature is not supported by some servers.</span></span> <span data-ttu-id="4ee27-107">例如，不支援對 Hyper-v 主控台會話的連線，而且可能需要停用預設值以支援同盟驗證。</span><span class="sxs-lookup"><span data-stu-id="4ee27-107">For example, this is not supported for connections to Hyper-V console sessions, and it may be necessary to disable the default to support federated authentication.</span></span> <span data-ttu-id="4ee27-108">在這些情況下，您可以藉由建立下列登錄機碼來停用這項功能，以允許連線通過。</span><span class="sxs-lookup"><span data-stu-id="4ee27-108">In these cases, this feature can be disabled by creating the following registry key to allow connections to go through.</span></span>

<span data-ttu-id="4ee27-109">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 終端機伺服器閘道 \\ preRDPDisableRegKey**</span><span class="sxs-lookup"><span data-stu-id="4ee27-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server Gateway\\preRDPDisableRegKey**</span></span>

<span data-ttu-id="4ee27-110">當此機碼存在時，遠端桌面閘道將不會強制執行裝置重新導向。</span><span class="sxs-lookup"><span data-stu-id="4ee27-110">When this key exists, the Remote Desktop Gateway will not enforce device redirection.</span></span>

 

 





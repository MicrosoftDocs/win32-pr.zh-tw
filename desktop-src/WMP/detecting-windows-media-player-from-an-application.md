---
title: 從應用程式偵測 Windows Media Player
description: 從應用程式偵測 Windows Media Player
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player，從應用程式偵測
- 從應用程式偵測 Windows Media Player
- 登錄，從應用程式偵測 Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967845"
---
# <a name="detecting-windows-media-player-from-an-application"></a><span data-ttu-id="b3421-106">從應用程式偵測 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="b3421-106">Detecting Windows Media Player from an Application</span></span>

<span data-ttu-id="b3421-107">您可以藉由檢查下列登錄機碼來判斷安裝的 Windows Media Player 版本：</span><span class="sxs-lookup"><span data-stu-id="b3421-107">You can determine what version of Windows Media Player is installed by checking the following registry key:</span></span>

<span data-ttu-id="b3421-108">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Active Setup \\ 已安裝的元件**</span><span class="sxs-lookup"><span data-stu-id="b3421-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Active Setup\\Installed Components**</span></span>

<span data-ttu-id="b3421-109">針對 Windows Media Player 6.4，請查看金鑰 **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**。</span><span class="sxs-lookup"><span data-stu-id="b3421-109">For Windows Media Player 6.4, look at key **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.</span></span>

<span data-ttu-id="b3421-110">針對 Windows Media Player 7 或更新版本，請查看金鑰 **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**。</span><span class="sxs-lookup"><span data-stu-id="b3421-110">For Windows Media Player 7 or later, look at key **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**.</span></span>

<span data-ttu-id="b3421-111">在上述任一機碼下，如果 **IsInstalled**</span><span class="sxs-lookup"><span data-stu-id="b3421-111">Under either of these keys, if the **IsInstalled**</span></span><dl> <dt>

<span data-ttu-id="b3421-112">資料類型</span><span class="sxs-lookup"><span data-stu-id="b3421-112">Data type</span></span>
</dt> <dd><span data-ttu-id="b3421-113">DWORD</span><span class="sxs-lookup"><span data-stu-id="b3421-113">DWORD</span></span></dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

<span data-ttu-id="b3421-114">資料類型</span><span class="sxs-lookup"><span data-stu-id="b3421-114">Data type</span></span>
</dt> <dd><span data-ttu-id="b3421-115">字串</span><span class="sxs-lookup"><span data-stu-id="b3421-115">string</span></span></dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a><span data-ttu-id="b3421-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3421-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3421-117">**轉散發 Windows Media Player 軟體**</span><span class="sxs-lookup"><span data-stu-id="b3421-117">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 





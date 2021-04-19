---
title: 無訊息取得登錄設定
description: 無訊息取得登錄設定
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106988020"
---
# <a name="silent-acquisition-registry-setting"></a><span data-ttu-id="672b3-103">無訊息取得登錄設定</span><span class="sxs-lookup"><span data-stu-id="672b3-103">Silent Acquisition Registry Setting</span></span>

<span data-ttu-id="672b3-104">Microsoft Windows Media Player 會使用下列登錄值來判斷是否要啟用無訊息取得，這是當使用者播放或同步受保護的內容時，播放玩家自動下載許可權的狀態。</span><span class="sxs-lookup"><span data-stu-id="672b3-104">Microsoft Windows Media Player uses the following registry value to determine whether to enable silent acquisition, a state in which the player downloads usage rights automatically when the user plays or syncs protected content.</span></span>

<span data-ttu-id="672b3-105">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **MediaPlayer** \\ **喜好** 設定 \\ **SilentAcquisition**</span><span class="sxs-lookup"><span data-stu-id="672b3-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**MediaPlayer**\\**Preferences**\\**SilentAcquisition**</span></span>

<span data-ttu-id="672b3-106">SilentAcquisition 值的格式如下：</span><span class="sxs-lookup"><span data-stu-id="672b3-106">The SilentAcquisition value has the following form:</span></span>



| <span data-ttu-id="672b3-107">名稱</span><span class="sxs-lookup"><span data-stu-id="672b3-107">Name</span></span>              | <span data-ttu-id="672b3-108">類型</span><span class="sxs-lookup"><span data-stu-id="672b3-108">Type</span></span>           | <span data-ttu-id="672b3-109">Description</span><span class="sxs-lookup"><span data-stu-id="672b3-109">Description</span></span>                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="672b3-110">SilentAcquisition</span><span class="sxs-lookup"><span data-stu-id="672b3-110">SilentAcquisition</span></span> | <span data-ttu-id="672b3-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="672b3-111">**REG\_DWORD**</span></span> | <span data-ttu-id="672b3-112">將此值設定為1，以啟用無訊息取得，或將它設定為0以停用無訊息取得。</span><span class="sxs-lookup"><span data-stu-id="672b3-112">Set this value to 1 to enable silent acquisition, or set it to 0 to disable silent acquisition.</span></span> <span data-ttu-id="672b3-113">預設值是 1。</span><span class="sxs-lookup"><span data-stu-id="672b3-113">The default is 1.</span></span> |



 

<span data-ttu-id="672b3-114">若要指定值，使用者可以開始 Windows Media Player，開啟 [ **選項** ] 對話方塊，按一下 [ **隱私權** ] 索引標籤，然後選取或清除 [ **當我播放或同步處理檔案時自動下載許可權** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="672b3-114">To specify a value, the user can start Windows Media Player, open the **Options** dialog box, click the **Privacy** tab, and then select or clear the **Download usage rights automatically when I play or sync a file** check box.</span></span> <span data-ttu-id="672b3-115">選取此核取方塊會將 SilentAcquisition 設定為 1;清除此核取方塊會將它設定為0。</span><span class="sxs-lookup"><span data-stu-id="672b3-115">Selecting this check box sets SilentAcquisition to 1; clearing the check box sets it to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="672b3-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="672b3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="672b3-117">**登錄設定**</span><span class="sxs-lookup"><span data-stu-id="672b3-117">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 





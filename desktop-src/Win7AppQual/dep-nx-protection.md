---
description: .
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: DEP/NX 保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c4a4cedead32504b6b78ba34bb72ee6b2ef400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852639"
---
# <a name="depnx-protection"></a><span data-ttu-id="fee90-103">DEP/NX 保護</span><span class="sxs-lookup"><span data-stu-id="fee90-103">DEP/NX Protection</span></span>

<span data-ttu-id="fee90-104">從 windows Vista 上的 Windows Internet Explorer 7 開始，[網際網路控制台] 專案包含了 [ **啟用記憶體保護** ] 選項，可協助減輕線上攻擊的風險。</span><span class="sxs-lookup"><span data-stu-id="fee90-104">Starting with Windows Internet Explorer 7 on Windows Vista, the Internet control panel item includes an **Enable memory protection** option to help mitigate online attacks.</span></span> <span data-ttu-id="fee90-105">此選項也稱為「 *資料執行防護* 」 (DEP) 或「 *不執行* 」 (NX) 。</span><span class="sxs-lookup"><span data-stu-id="fee90-105">This option is also referred to as *Data Execution Prevention* (DEP) or *No-Execute* (NX).</span></span> <span data-ttu-id="fee90-106">啟用此選項時，它會與處理器搭配運作，藉由封鎖標記為無法執行的記憶體中的程式碼執行，以協助防止緩衝區溢位攻擊。</span><span class="sxs-lookup"><span data-stu-id="fee90-106">When this option is enabled, it works with the processor to help prevent buffer overflow attacks by blocking code execution from memory that is marked as non-executable.</span></span>

<span data-ttu-id="fee90-107">在 windows Vista （含 Service Pack 1） (SP1) 作業系統或更新版本的 windows Internet Explorer 8 中，預設會啟用此選項。</span><span class="sxs-lookup"><span data-stu-id="fee90-107">In Windows Internet Explorer 8 on the Windows Vista with Service Pack 1 (SP1) operating system or a later version, this option is enabled by default.</span></span> <span data-ttu-id="fee90-108">DEP/NX 無法防止所有以記憶體為基礎的弱點。</span><span class="sxs-lookup"><span data-stu-id="fee90-108">DEP/NX does not protect against all memory-based vulnerabilities.</span></span> <span data-ttu-id="fee90-109">但是，當它與其他技術（例如位址空間配置隨機載入）結合 (ASLR) 時，它有助於防止 Windows Internet Explorer 中常見的緩衝區溢位弱點，以及它所載入的增益集。</span><span class="sxs-lookup"><span data-stu-id="fee90-109">But when it is combined with other technologies like Address Space Layout Randomization (ASLR), it helps prevent common buffer overflow vulnerabilities in Windows Internet Explorer and the add-ons that it loads.</span></span> <span data-ttu-id="fee90-110">不需要額外的使用者互動來提供此保護，也不會引進任何新的提示。</span><span class="sxs-lookup"><span data-stu-id="fee90-110">No additional user interaction is required to provide this protection, and no new prompts are introduced.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fee90-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="fee90-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fee90-112">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="fee90-112">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 




---
title: BITS ADSI 擴充功能
description: BITS 伺服器提供下列 ADSI 擴充介面，以啟用 BITS 上傳。
ms.assetid: 7937a86d-886b-4764-bfc1-2ffd64dbcbc1
keywords:
- BITS ADSI 擴充功能位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c045f8f7fff8e66251a94a9f704046674934ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967402"
---
# <a name="bits-adsi-extension"></a><span data-ttu-id="4f053-104">BITS ADSI 擴充功能</span><span class="sxs-lookup"><span data-stu-id="4f053-104">BITS ADSI Extension</span></span>

<span data-ttu-id="4f053-105">BITS 伺服器提供下列 ADSI 擴充介面，以啟用 BITS 上傳。</span><span class="sxs-lookup"><span data-stu-id="4f053-105">The BITS server provides the following ADSI extension interfaces to enable BITS uploads.</span></span>



| <span data-ttu-id="4f053-106">介面</span><span class="sxs-lookup"><span data-stu-id="4f053-106">Interface</span></span>                                                        | <span data-ttu-id="4f053-107">描述</span><span class="sxs-lookup"><span data-stu-id="4f053-107">Description</span></span>                                                                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f053-108">**IBITSExtensionSetup**</span><span class="sxs-lookup"><span data-stu-id="4f053-108">**IBITSExtensionSetup**</span></span>](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup)               | <span data-ttu-id="4f053-109">用來啟用和停用 BITS 上傳至虛擬目錄。</span><span class="sxs-lookup"><span data-stu-id="4f053-109">Use to enable and disable BITS uploads to a virtual directory.</span></span>                                                                                 |
| [<span data-ttu-id="4f053-110">**IBITSExtensionSetupFactory**</span><span class="sxs-lookup"><span data-stu-id="4f053-110">**IBITSExtensionSetupFactory**</span></span>](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetupfactory) | <span data-ttu-id="4f053-111">用來在安裝 BITS 伺服器的安裝程式中，取得 [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4f053-111">Use to retrieve a pointer to an [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) interface in a setup program that installs the BITS server.</span></span> |



 

 

 





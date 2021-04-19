---
description: CVideoCaptureTerminal 終端機衍生自 CSingleFilterTerminal，並使用單一的 DirectShow 篩選器來實行靜態影片捕獲終端機。
ms.assetid: e66b1c8d-37c0-40c7-8ad6-b1e84294b02b
title: CVideoCaptureTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d89aad45b6ca58200a2dcbf0fd020b59cda54bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970180"
---
# <a name="cvideocaptureterminal"></a><span data-ttu-id="9d3da-103">CVideoCaptureTerminal</span><span class="sxs-lookup"><span data-stu-id="9d3da-103">CVideoCaptureTerminal</span></span>

<span data-ttu-id="9d3da-104">**CVideoCaptureTerminal** 終端機衍生自 [CSingleFilterTerminal](csinglefilterterminal.md) ，並使用單一的 DirectShow 篩選器來實行靜態影片捕獲終端機。</span><span class="sxs-lookup"><span data-stu-id="9d3da-104">The **CVideoCaptureTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static video capture terminal using a single DirectShow filter.</span></span> <span data-ttu-id="9d3da-105">它不支援僅適用于 WDM 影片捕獲的某些 advanced video capture 介面。</span><span class="sxs-lookup"><span data-stu-id="9d3da-105">It does not support certain advanced video capture interfaces that are applicable only to WDM video capture.</span></span> <span data-ttu-id="9d3da-106">大部分的 Msp 都不需要覆寫此終端機的執行。</span><span class="sxs-lookup"><span data-stu-id="9d3da-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="9d3da-107">定義于 MSPtmvc 中。</span><span class="sxs-lookup"><span data-stu-id="9d3da-107">Defined in MSPtmvc.h.</span></span>

 

 




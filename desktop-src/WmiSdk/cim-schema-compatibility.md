---
description: CIM 架構相容性
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: CIM 架構相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df559469ef6a8284b51951dc365bad6c302ca865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981197"
---
# <a name="cim-schema-compatibility"></a><span data-ttu-id="e5522-103">CIM 架構相容性</span><span class="sxs-lookup"><span data-stu-id="e5522-103">CIM Schema Compatibility</span></span>

<span data-ttu-id="e5522-104">Windows Management Instrumentation (WMI) 基礎結構的重要元件，是系統中可管理之實體的面向物件模型。</span><span class="sxs-lookup"><span data-stu-id="e5522-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="e5522-105">此模型符合桌面管理工作強制 ([DMTF](https://www.dmtf.org/standards/wsman)) 所維護的標準，也稱為通用訊息模型 (CIM) 。</span><span class="sxs-lookup"><span data-stu-id="e5522-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="e5522-106">CIM 架構會為其提供的任何資料提供單一資料描述機制。</span><span class="sxs-lookup"><span data-stu-id="e5522-106">The CIM schema provides a single data description mechanism for any data that they provide.</span></span>

<span data-ttu-id="e5522-107">從 Windows 7 開始，WMI 與 CIM 架構版本 2.17.1 ([https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171)) 相容。</span><span class="sxs-lookup"><span data-stu-id="e5522-107">Starting in Windows 7, WMI is compatible with the CIM Schema version 2.17.1 ([https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171)).</span></span> <span data-ttu-id="e5522-108">使用者現在可以在 Windows 電腦上編譯 DMTF 定義的架構。</span><span class="sxs-lookup"><span data-stu-id="e5522-108">Users can now compile a DMTF defined schema on a Windows computer.</span></span>

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a><span data-ttu-id="e5522-109">CIM 架構版本2.17.1 相容性的優點</span><span class="sxs-lookup"><span data-stu-id="e5522-109">Benefits of CIM Schema version 2.17.1 compatibility</span></span>

-   <span data-ttu-id="e5522-110">當使用者下載 CIM 架構版本2.17.1 或 DMTF MOF 檔案時，可以在目標 Windows 電腦上順利編譯。</span><span class="sxs-lookup"><span data-stu-id="e5522-110">When a user downloads CIM Schema version 2.17.1 or DMTF MOF files, they can be successfully compiled on the target Windows computer.</span></span>
-   <span data-ttu-id="e5522-111">CIM 架構版本2.17.1 新增了對 BIOS、印表機、標準訊息、作業系統狀態、新式電源管理範例、虛擬化和安全性的支援。</span><span class="sxs-lookup"><span data-stu-id="e5522-111">The CIM Schema version 2.17.1 added support for BIOS, printers, standard messages, operating system state, modern power management paradigms, virtualization and security.</span></span>
-   <span data-ttu-id="e5522-112">CIM 架構版本2.1.7.1 提供其他設定檔支援。</span><span class="sxs-lookup"><span data-stu-id="e5522-112">CIM Schema version 2.1.7.1 offers additional profile support.</span></span> <span data-ttu-id="e5522-113">如需詳細資訊，請參閱 [跨命名空間關聯的遍歷](cross-namespace-association-traversal.md)</span><span class="sxs-lookup"><span data-stu-id="e5522-113">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md)</span></span>

 

 




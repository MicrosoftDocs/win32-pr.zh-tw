---
description: 瞭解 PrintCapabilities 的用途。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: 使用 PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09882d42814930ef5ba08e087f1df87e0d0e9bc
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119423"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="5b2d1-105">使用 PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="5b2d1-105">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="5b2d1-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="5b2d1-106">This topic is not current.</span></span> <span data-ttu-id="5b2d1-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="5b2d1-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5b2d1-108">PrintCapabilities 的目的是要將可設定的裝置屬性工作表示為功能/選項結構或參數結構。</span><span class="sxs-lookup"><span data-stu-id="5b2d1-108">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="5b2d1-109">這項資訊會定義裝置的設定空間，並且可供使用者介面 (UI) 用戶端用來建立 UI。</span><span class="sxs-lookup"><span data-stu-id="5b2d1-109">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="5b2d1-110">Print Schema 關鍵字會定義一組標準功能實例、標準功能實例的選項實例，以及 ParameterDef 實例。</span><span class="sxs-lookup"><span data-stu-id="5b2d1-110">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="5b2d1-111">PrintCapabilities 中的功能/選項或參數結構旨在保存描述裝置的屬性或 ScoredProperty 實例，以及多工緩衝處理器子系統所支援的實例。</span><span class="sxs-lookup"><span data-stu-id="5b2d1-111">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="5b2d1-112">這些屬性和 ScoredProperty 實例是裝置用戶端的一般興趣，並包含 Win32 DevCaps 函式所提供的資訊。</span><span class="sxs-lookup"><span data-stu-id="5b2d1-112">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="5b2d1-113">Print Schema 關鍵字會定義一組標準屬性和 ScoredProperty 實例。</span><span class="sxs-lookup"><span data-stu-id="5b2d1-113">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="5b2d1-114">請注意，PrintCapabilities 檔的目的是只代表單一值資料：不相依于裝置特定設定的資料。</span><span class="sxs-lookup"><span data-stu-id="5b2d1-114">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="5b2d1-115">PrintCapabilities 檔只提供設定相依資料的快照集。</span><span class="sxs-lookup"><span data-stu-id="5b2d1-115">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b2d1-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b2d1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b2d1-117">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="5b2d1-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




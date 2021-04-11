---
description: 深入瞭解：封包 API 結構
ms.assetid: b6d636e6-2af0-427c-a529-56c80b349b58
title: 封包 API 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6acae2a62d59353e10eb07e0e3f25e763b69eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025894"
---
# <a name="cabinet-api-structures"></a><span data-ttu-id="68bf3-103">封包 API 結構</span><span class="sxs-lookup"><span data-stu-id="68bf3-103">Cabinet API Structures</span></span>

<span data-ttu-id="68bf3-104">本節詳細說明下列封包 API 結構：</span><span class="sxs-lookup"><span data-stu-id="68bf3-104">This section details the following Cabinet API Structures:</span></span>



| <span data-ttu-id="68bf3-105">結構</span><span class="sxs-lookup"><span data-stu-id="68bf3-105">Structure</span></span>                                              | <span data-ttu-id="68bf3-106">Description</span><span class="sxs-lookup"><span data-stu-id="68bf3-106">Description</span></span>                                                                                     |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68bf3-107">**CABINETDLLVERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="68bf3-107">**CABINETDLLVERSIONINFO**</span></span>](cabinetdllversioninfo.md) | <span data-ttu-id="68bf3-108">包含 Cabinet.dll 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="68bf3-108">Contains the version information for Cabinet.dll.</span></span><br/>                                    |
| [<span data-ttu-id="68bf3-109">**CCAB**</span><span class="sxs-lookup"><span data-stu-id="68bf3-109">**CCAB**</span></span>](/windows/desktop/api/Fci/ns-fci-ccab)                                   | <span data-ttu-id="68bf3-110">包含封包資訊。</span><span class="sxs-lookup"><span data-stu-id="68bf3-110">Contains cabinet information.</span></span><br/>                                                        |
| [<span data-ttu-id="68bf3-111">**ERF**</span><span class="sxs-lookup"><span data-stu-id="68bf3-111">**ERF**</span></span>](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)                                     | <span data-ttu-id="68bf3-112">從 FCI/FDI 傳回錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="68bf3-112">Returns error information from FCI/FDI.</span></span> <span data-ttu-id="68bf3-113">呼叫端不應該修改此結構。</span><span class="sxs-lookup"><span data-stu-id="68bf3-113">The caller should not modify this structure.</span></span><br/> |
| [<span data-ttu-id="68bf3-114">**FDICABINETINFO**</span><span class="sxs-lookup"><span data-stu-id="68bf3-114">**FDICABINETINFO**</span></span>](/windows/desktop/api/Fdi/ns-fdi-fdicabinetinfo)               | <span data-ttu-id="68bf3-115">包含特定封包檔的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="68bf3-115">Contains details about a particular cabinet file.</span></span><br/>                                    |
| [<span data-ttu-id="68bf3-116">**FDINOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="68bf3-116">**FDINOTIFICATION**</span></span>](/windows/desktop/api/Fdi/ns-fdi-fdinotification)             | <span data-ttu-id="68bf3-117">提供資訊給 [**FNFDINOTIFY**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify)。</span><span class="sxs-lookup"><span data-stu-id="68bf3-117">Provide information to [**FNFDINOTIFY**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify).</span></span><br/>                           |
| [<span data-ttu-id="68bf3-118">**會話**</span><span class="sxs-lookup"><span data-stu-id="68bf3-118">**SESSION**</span></span>](session.md)                             | <span data-ttu-id="68bf3-119">包含目前會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="68bf3-119">Contains information about the current session.</span></span><br/>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="68bf3-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="68bf3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68bf3-121">封包 API 參考</span><span class="sxs-lookup"><span data-stu-id="68bf3-121">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="68bf3-122">使用封包 API</span><span class="sxs-lookup"><span data-stu-id="68bf3-122">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 

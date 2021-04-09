---
title: 'WINBIO_ENG_CAP 常數 (Winbio \_ 類型 .h) '
description: 指定一般引擎功能。
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d69db9f0e15ca0d50aa5ca134fdc74904dec85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686515"
---
# <a name="winbio_eng_cap-constants"></a><span data-ttu-id="dc167-103">WINBIO \_ ENG \_ CAP 常數</span><span class="sxs-lookup"><span data-stu-id="dc167-103">WINBIO\_ENG\_CAP Constants</span></span>

<span data-ttu-id="dc167-104">下列常數是 **WINBIO 的 \_ 功能** 值，可用來指定連接到特定生物特徵辨識單位之引擎元件的一般功能。</span><span class="sxs-lookup"><span data-stu-id="dc167-104">The following constants are **WINBIO\_CAPABILITIES** values that can be used to specify generic capabilities of the engine component that is connected to a specific biometric unit.</span></span> <span data-ttu-id="dc167-105">您可以在 [**WINBIO \_ 擴充 \_ 引擎 \_ 資訊**](winbio-extended-engine-info.md)結構的 **GenericEngineCapabilities** 成員中指定這些功能。</span><span class="sxs-lookup"><span data-stu-id="dc167-105">You specify these capabilities in **GenericEngineCapabilities** member of the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure.</span></span>



| <span data-ttu-id="dc167-106">常數/值</span><span class="sxs-lookup"><span data-stu-id="dc167-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="dc167-107">Description</span><span class="sxs-lookup"><span data-stu-id="dc167-107">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <span data-ttu-id="dc167-108"><dt>**WINBIO \_ENG \_ 上限 \_ 反復 \_ 改進**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="dc167-108"><dt>**WINBIO\_ENG\_CAP\_ITERATIVE\_IMPROVEMENT**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="dc167-109">生物特徵辨識引擎元件可以執行反復的改進。</span><span class="sxs-lookup"><span data-stu-id="dc167-109">The biometric engine component can perform iterative improvement.</span></span><br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <span data-ttu-id="dc167-110"><dt>**WINBIO \_ENG \_ 上限 \_ 詐騙 \_ 偵測**</dt>到 <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="dc167-110"><dt>**WINBIO\_ENG\_CAP\_SPOOF\_DETECTION**</dt> <dt>0x00000002</dt></span></span> </dl>                   | <span data-ttu-id="dc167-111">生物識別引擎元件可以執行欺騙偵測。</span><span class="sxs-lookup"><span data-stu-id="dc167-111">The biometric engine component can perform spoof detection.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="dc167-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc167-112">Requirements</span></span>



| <span data-ttu-id="dc167-113">需求</span><span class="sxs-lookup"><span data-stu-id="dc167-113">Requirement</span></span> | <span data-ttu-id="dc167-114">值</span><span class="sxs-lookup"><span data-stu-id="dc167-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc167-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc167-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dc167-116">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc167-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="dc167-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc167-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dc167-118">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc167-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dc167-119">標頭</span><span class="sxs-lookup"><span data-stu-id="dc167-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc167-120"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dc167-120"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 






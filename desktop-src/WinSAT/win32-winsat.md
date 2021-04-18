---
title: Win32_WinSAT 類別
description: 定義最新正式評量的摘要評估資訊。
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Win32_WinSAT 類別 WinSAT
- Win32_WinSAT 類別 WinSAT，描述
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965122"
---
# <a name="win32_winsat-class"></a><span data-ttu-id="6989e-105">Win32 \_ WinSAT 類別</span><span class="sxs-lookup"><span data-stu-id="6989e-105">Win32\_WinSAT class</span></span>

<span data-ttu-id="6989e-106">\[**Win32 \_** 在 Windows 8.1 之後，可能會變更或無法使用 WinSAT。\]</span><span class="sxs-lookup"><span data-stu-id="6989e-106">\[**Win32\_WinSAT** may be altered or unavailable for releases after Windows 8.1.\]</span></span>

<span data-ttu-id="6989e-107">定義最新正式評量的摘要評估資訊。</span><span class="sxs-lookup"><span data-stu-id="6989e-107">Defines summary assessment information for the most recent formal assessment.</span></span>

<span data-ttu-id="6989e-108">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6989e-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6989e-109">語法</span><span class="sxs-lookup"><span data-stu-id="6989e-109">Syntax</span></span>

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a><span data-ttu-id="6989e-110">成員</span><span class="sxs-lookup"><span data-stu-id="6989e-110">Members</span></span>

<span data-ttu-id="6989e-111">**Win32 \_ WinSAT** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6989e-111">The **Win32\_WinSAT** class has these types of members:</span></span>

-   [<span data-ttu-id="6989e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="6989e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6989e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="6989e-113">Properties</span></span>

<span data-ttu-id="6989e-114">**Win32 \_ WinSAT** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6989e-114">The **Win32\_WinSAT** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6989e-115">**CPUScore**</span><span class="sxs-lookup"><span data-stu-id="6989e-115">**CPUScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6989e-116">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="6989e-116">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6989e-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6989e-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6989e-118">電腦上的處理器分數。</span><span class="sxs-lookup"><span data-stu-id="6989e-118">A score for the processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="6989e-119">**D3DScore**</span><span class="sxs-lookup"><span data-stu-id="6989e-119">**D3DScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6989e-120">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="6989e-120">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6989e-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6989e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6989e-122">在 Windows 8.1 之後，WinSAT 就不會再評估三維圖形 (電腦的遊戲) 功能，以及圖形驅動程式使用此評量轉譯物件和執行著色器的能力。</span><span class="sxs-lookup"><span data-stu-id="6989e-122">After Windows 8.1, WinSAT no longer assess the three-dimensional graphics (gaming) capabilities of the computer and the graphics driver's ability to render objects and execute shaders using this assessment.</span></span> <span data-ttu-id="6989e-123">為了提供相容性，WinSAT 會報告計量和分數的 sentinel 值，但不會即時計算這些值。</span><span class="sxs-lookup"><span data-stu-id="6989e-123">For compatibility, WinSAT report sentinel values for the metrics and scores, however these are not calculated in real time.</span></span>

</dd> <dt>

<span data-ttu-id="6989e-124">**DiskScore**</span><span class="sxs-lookup"><span data-stu-id="6989e-124">**DiskScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6989e-125">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="6989e-125">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6989e-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6989e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6989e-127">電腦上主要硬碟的連續讀取輸送量分數。</span><span class="sxs-lookup"><span data-stu-id="6989e-127">A score for the sequential read throughput on the primary hard disk on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="6989e-128">**GraphicsScore**</span><span class="sxs-lookup"><span data-stu-id="6989e-128">**GraphicsScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6989e-129">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="6989e-129">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6989e-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6989e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6989e-131">電腦圖形功能的分數。</span><span class="sxs-lookup"><span data-stu-id="6989e-131">A score for the graphics capabilities of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="6989e-132">**MemoryScore**</span><span class="sxs-lookup"><span data-stu-id="6989e-132">**MemoryScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6989e-133">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="6989e-133">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6989e-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6989e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6989e-135">電腦的記憶體輸送量和容量分數。</span><span class="sxs-lookup"><span data-stu-id="6989e-135">A score for the memory throughput and capacity of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="6989e-136">**TimeTaken**</span><span class="sxs-lookup"><span data-stu-id="6989e-136">**TimeTaken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6989e-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6989e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6989e-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6989e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6989e-139">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="6989e-139">Qualifiers: **key**</span></span>
</dt> </dl>

<span data-ttu-id="6989e-140">在 WQL 查詢的 WHERE 子句中，這個屬性必須設定為 "MostRecentAssessment"。</span><span class="sxs-lookup"><span data-stu-id="6989e-140">This property must be set to "MostRecentAssessment" in the WHERE clause of your WQL query.</span></span>

</dd> <dt>

<span data-ttu-id="6989e-141">**WinSATAssessmentState**</span><span class="sxs-lookup"><span data-stu-id="6989e-141">**WinSATAssessmentState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6989e-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6989e-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6989e-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6989e-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6989e-144">評量的狀態。</span><span class="sxs-lookup"><span data-stu-id="6989e-144">State of the assessment.</span></span> <span data-ttu-id="6989e-145">如需可能值的描述，請參閱 [**WINSAT \_ 評定 \_ 狀態**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) 列舉。</span><span class="sxs-lookup"><span data-stu-id="6989e-145">For a description of the possible values, see the [**WINSAT\_ASSESSMENT\_STATE**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="6989e-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0) </span><span class="sxs-lookup"><span data-stu-id="6989e-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6989e-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**有效** (1) </span><span class="sxs-lookup"><span data-stu-id="6989e-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Valid** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6989e-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2) </span><span class="sxs-lookup"><span data-stu-id="6989e-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6989e-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3) </span><span class="sxs-lookup"><span data-stu-id="6989e-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6989e-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**無效** 的 (4) </span><span class="sxs-lookup"><span data-stu-id="6989e-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6989e-151">**WinSPRLevel**</span><span class="sxs-lookup"><span data-stu-id="6989e-151">**WinSPRLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6989e-152">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="6989e-152">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6989e-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6989e-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6989e-154">電腦的基本分數。</span><span class="sxs-lookup"><span data-stu-id="6989e-154">Base score for the computer.</span></span> <span data-ttu-id="6989e-155">如需分數值的詳細資訊，請參閱 [**IProvideWinSATResultsInfo：： SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) 屬性。</span><span class="sxs-lookup"><span data-stu-id="6989e-155">For details on the score value, see the [**IProvideWinSATResultsInfo::SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6989e-156">備註</span><span class="sxs-lookup"><span data-stu-id="6989e-156">Remarks</span></span>

<span data-ttu-id="6989e-157">如需子元件分數（例如 **MemoryScore**）的詳細資訊，請參閱 [**IProvideWinSATAssessmentInfo：：計分**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) 屬性。</span><span class="sxs-lookup"><span data-stu-id="6989e-157">For information on the subcomponent scores, such as **MemoryScore**, see the [**IProvideWinSATAssessmentInfo::Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) property.</span></span>

## <a name="examples"></a><span data-ttu-id="6989e-158">範例</span><span class="sxs-lookup"><span data-stu-id="6989e-158">Examples</span></span>

<span data-ttu-id="6989e-159">如需示範如何使用 WMI 從這個類別取出資料的範例，請參閱 [**IProvideWinSATVisuals：： get \_ Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) 方法。</span><span class="sxs-lookup"><span data-stu-id="6989e-159">For an example that shows how to use WMI to retrieve data from this class, see the [**IProvideWinSATVisuals::get\_Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6989e-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="6989e-160">Requirements</span></span>



| <span data-ttu-id="6989e-161">需求</span><span class="sxs-lookup"><span data-stu-id="6989e-161">Requirement</span></span> | <span data-ttu-id="6989e-162">值</span><span class="sxs-lookup"><span data-stu-id="6989e-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6989e-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6989e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="6989e-164">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6989e-164">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6989e-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6989e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="6989e-166">都不支援</span><span class="sxs-lookup"><span data-stu-id="6989e-166">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6989e-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="6989e-167">Namespace</span></span><br/>                | <span data-ttu-id="6989e-168">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6989e-168">Root\\CIMv2</span></span><br/>                                                                   |
| <span data-ttu-id="6989e-169">MOF</span><span class="sxs-lookup"><span data-stu-id="6989e-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6989e-170"><dt>WinSAT. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6989e-170"><dt>WinSAT.mof</dt></span></span> </dl>    |
| <span data-ttu-id="6989e-171">DLL</span><span class="sxs-lookup"><span data-stu-id="6989e-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6989e-172"><dt>WinSATAPI.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6989e-172"><dt>WinSATAPI.dll</dt></span></span> </dl> |



 

 






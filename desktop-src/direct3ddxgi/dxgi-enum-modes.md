---
description: 列舉顯示模式的選項。
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: 'DXGI_ENUM_MODES (DXGI. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992309"
---
# <a name="dxgi_enum_modes"></a><span data-ttu-id="d0c0a-103">DXGI \_ 列舉 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="d0c0a-103">DXGI\_ENUM\_MODES</span></span>

<span data-ttu-id="d0c0a-104">列舉顯示模式的選項。</span><span class="sxs-lookup"><span data-stu-id="d0c0a-104">Options for enumerating display modes.</span></span>



| <span data-ttu-id="d0c0a-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="d0c0a-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="d0c0a-106">Description</span><span class="sxs-lookup"><span data-stu-id="d0c0a-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <span data-ttu-id="d0c0a-107"><dt>**DXGI \_列舉 \_ 模式 \_ 交錯**</dt>式 <dt>1UL</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0a-107"><dt>**DXGI\_ENUM\_MODES\_INTERLACED**</dt> <dt>1UL</dt></span></span> </dl>                 | <span data-ttu-id="d0c0a-108">包含交錯模式。</span><span class="sxs-lookup"><span data-stu-id="d0c0a-108">Include interlaced modes.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <span data-ttu-id="d0c0a-109"><dt>**DXGI \_列舉 \_ 模式 \_ 調整**</dt> <dt>2UL</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0a-109"><dt>**DXGI\_ENUM\_MODES\_SCALING**</dt> <dt>2UL</dt></span></span> </dl>                          | <span data-ttu-id="d0c0a-110">包含延伸調整模式。</span><span class="sxs-lookup"><span data-stu-id="d0c0a-110">Include stretched-scaling modes.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <span data-ttu-id="d0c0a-111"><dt>**DXGI \_列舉 \_ 模式 \_ 身歷聲**</dt> <dt>4UL</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0a-111"><dt>**DXGI\_ENUM\_MODES\_STEREO**</dt> <dt>4UL</dt></span></span> </dl>                             | <span data-ttu-id="d0c0a-112">包含身歷聲模式。</span><span class="sxs-lookup"><span data-stu-id="d0c0a-112">Include stereo modes.</span></span><br/> <span data-ttu-id="d0c0a-113">**Direct3D 11：** 從 Windows 8 開始支援這個列舉值。</span><span class="sxs-lookup"><span data-stu-id="d0c0a-113">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <span data-ttu-id="d0c0a-114"><dt>**DXGI \_\_ \_ 已停用 \_ 的列舉模式身歷聲**</dt> <dt>8UL</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0a-114"><dt>**DXGI\_ENUM\_MODES\_DISABLED\_STEREO**</dt> <dt>8UL</dt></span></span> </dl> | <span data-ttu-id="d0c0a-115">包含因為使用者已停用身歷聲而隱藏的立體模式。</span><span class="sxs-lookup"><span data-stu-id="d0c0a-115">Include stereo modes that are hidden because the user has disabled stereo.</span></span> <span data-ttu-id="d0c0a-116">[控制台] 應用程式可以使用此選項，顯示在啟用和停用身歷聲的使用者介面中，已停用的立體功能。</span><span class="sxs-lookup"><span data-stu-id="d0c0a-116">Control panel applications can use this option to show stereo capabilities that have been disabled as part of a user interface that enables and disables stereo.</span></span><br/> <span data-ttu-id="d0c0a-117">**Direct3D 11：** 從 Windows 8 開始支援這個列舉值。</span><span class="sxs-lookup"><span data-stu-id="d0c0a-117">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d0c0a-118">備註</span><span class="sxs-lookup"><span data-stu-id="d0c0a-118">Remarks</span></span>

<span data-ttu-id="d0c0a-119">[**IDXGIOutput：： GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist)中使用這些旗標選項來列舉顯示模式。</span><span class="sxs-lookup"><span data-stu-id="d0c0a-119">These flag options are used in [**IDXGIOutput::GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) to enumerate display modes.</span></span>

<span data-ttu-id="d0c0a-120">[**IDXGIOutput1：： GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1)也會使用這些旗標選項來列舉顯示模式。</span><span class="sxs-lookup"><span data-stu-id="d0c0a-120">These flag options are also used in [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) to enumerate display modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c0a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0c0a-121">Requirements</span></span>



| <span data-ttu-id="d0c0a-122">需求</span><span class="sxs-lookup"><span data-stu-id="d0c0a-122">Requirement</span></span> | <span data-ttu-id="d0c0a-123">值</span><span class="sxs-lookup"><span data-stu-id="d0c0a-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d0c0a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d0c0a-124">Header</span></span><br/> | <dl> <span data-ttu-id="d0c0a-125"><dt>DXGI。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0c0a-125"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c0a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0c0a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c0a-127">DXGI 常數</span><span class="sxs-lookup"><span data-stu-id="d0c0a-127">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 





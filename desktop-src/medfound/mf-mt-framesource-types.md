---
description: 值，指出畫面格來源所提供的感應器類型，例如色彩、紅外線或深度。
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: 'MF_MT_FRAMESOURCE_TYPES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983395"
---
# <a name="mf_mt_framesource_types-attribute"></a><span data-ttu-id="cb4a2-103">MF \_ MT \_ FRAMESOURCE \_ 類型屬性</span><span class="sxs-lookup"><span data-stu-id="cb4a2-103">MF\_MT\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="cb4a2-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="cb4a2-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cb4a2-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="cb4a2-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cb4a2-106">值，指出畫面格來源所提供的感應器類型，例如色彩、紅外線或深度。</span><span class="sxs-lookup"><span data-stu-id="cb4a2-106">A value that indicates the type of sensor provided by a frame source, such as color, infrared, or depth.</span></span>

## <a name="data-type"></a><span data-ttu-id="cb4a2-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="cb4a2-107">Data type</span></span>

<span data-ttu-id="cb4a2-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cb4a2-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cb4a2-109">備註</span><span class="sxs-lookup"><span data-stu-id="cb4a2-109">Remarks</span></span>

<span data-ttu-id="cb4a2-110">此值應該是 [**\_ MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85))列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="cb4a2-110">This value should be a member of the [**\_MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) enumeration.</span></span> <span data-ttu-id="cb4a2-111">為了回溯相容性，在媒體類型上未定義此屬性時，會假設為 **\_ MFFrameSourceTyes：： Color**。</span><span class="sxs-lookup"><span data-stu-id="cb4a2-111">For backward compatibility, when this attribute is not defined on a media type, it's assumed to be **\_MFFrameSourceTyes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb4a2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb4a2-112">Requirements</span></span>



| <span data-ttu-id="cb4a2-113">需求</span><span class="sxs-lookup"><span data-stu-id="cb4a2-113">Requirement</span></span> | <span data-ttu-id="cb4a2-114">值</span><span class="sxs-lookup"><span data-stu-id="cb4a2-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4a2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb4a2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cb4a2-116">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb4a2-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cb4a2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb4a2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cb4a2-118">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb4a2-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="cb4a2-119">標頭</span><span class="sxs-lookup"><span data-stu-id="cb4a2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb4a2-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb4a2-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 

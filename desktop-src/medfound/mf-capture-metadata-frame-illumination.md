---
description: 值，指出框架是否使用主動紅外線 (IR) 照明來捕捉。
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: 'MF_CAPTURE_METADATA_FRAME_ILLUMINATION 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974129"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a><span data-ttu-id="80ba3-103">MF \_ 捕獲 \_ 中繼資料 \_ 框架 \_ 照明屬性</span><span class="sxs-lookup"><span data-stu-id="80ba3-103">MF\_CAPTURE\_METADATA\_FRAME\_ILLUMINATION attribute</span></span>

<span data-ttu-id="80ba3-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="80ba3-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="80ba3-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="80ba3-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="80ba3-106">值，指出框架是否使用主動紅外線 (IR) 照明來捕捉。</span><span class="sxs-lookup"><span data-stu-id="80ba3-106">A value indicating whether a frame was captured using active infrared (IR) illumination.</span></span>

## <a name="data-type"></a><span data-ttu-id="80ba3-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="80ba3-107">Data type</span></span>

<span data-ttu-id="80ba3-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="80ba3-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="80ba3-109">備註</span><span class="sxs-lookup"><span data-stu-id="80ba3-109">Remarks</span></span>

<span data-ttu-id="80ba3-110">這個屬性是位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="80ba3-110">This attribute is a bitmask.</span></span> <span data-ttu-id="80ba3-111">它是64位的值，可提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="80ba3-111">It is a 64 bit value for backward compatibility.</span></span>

<span data-ttu-id="80ba3-112">作用中的照明是當裝置有接近 IR 攝影機的燈光發射器發出燈光來照亮場景時，通常會發出 IR 燈，因此不會干擾人類眼睛。</span><span class="sxs-lookup"><span data-stu-id="80ba3-112">Active illumination is when a device has a light emitter close to the IR camera emitting a beam of light to illuminate the scene, typically emitting IR light so it won’t disturb human eyes.</span></span> <span data-ttu-id="80ba3-113">將值設定為 (值 & 0x1) ！ = 0 如果在使用中的照明時捕捉到框架，並將 (值設定為 & 0x1) = = 0 （如果作用中的照明已關閉）。</span><span class="sxs-lookup"><span data-stu-id="80ba3-113">Set value to (value & 0x1) != 0 if frame was captured when active illumination was on and set (value & 0x1) == 0 if active illumination was off.</span></span>

## <a name="requirements"></a><span data-ttu-id="80ba3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="80ba3-114">Requirements</span></span>



| <span data-ttu-id="80ba3-115">需求</span><span class="sxs-lookup"><span data-stu-id="80ba3-115">Requirement</span></span> | <span data-ttu-id="80ba3-116">值</span><span class="sxs-lookup"><span data-stu-id="80ba3-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80ba3-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80ba3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="80ba3-118">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80ba3-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="80ba3-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80ba3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="80ba3-120">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80ba3-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="80ba3-121">標頭</span><span class="sxs-lookup"><span data-stu-id="80ba3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="80ba3-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="80ba3-122"><dt>Mfapi.h</dt></span></span> </dl> |



 

 





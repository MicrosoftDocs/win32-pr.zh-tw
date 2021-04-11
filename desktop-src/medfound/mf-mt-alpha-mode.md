---
description: 指定彩色媒體影片類型的 Alpha 模式是預乘或直接。
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: 'MF_MT_ALPHA_MODE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026827"
---
# <a name="mf_mt_alpha_mode-attribute"></a><span data-ttu-id="c7bc3-103">MF \_ MT \_ ALPHA \_ 模式屬性</span><span class="sxs-lookup"><span data-stu-id="c7bc3-103">MF\_MT\_ALPHA\_MODE attribute</span></span>

<span data-ttu-id="c7bc3-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="c7bc3-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c7bc3-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="c7bc3-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c7bc3-106">指定彩色媒體影片類型的 Alpha 模式是預乘或直接。</span><span class="sxs-lookup"><span data-stu-id="c7bc3-106">Specifies whether the alpha mode for color media video types is premultiplied or straight.</span></span>

## <a name="data-type"></a><span data-ttu-id="c7bc3-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="c7bc3-107">Data type</span></span>

<span data-ttu-id="c7bc3-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c7bc3-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c7bc3-109">備註</span><span class="sxs-lookup"><span data-stu-id="c7bc3-109">Remarks</span></span>

<span data-ttu-id="c7bc3-110">這個值可以轉換成 [**DXGI \_ ALPHA \_ 模式**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) 值。</span><span class="sxs-lookup"><span data-stu-id="c7bc3-110">This value can be cast to a [**DXGI\_ALPHA\_MODE**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) value.</span></span> <span data-ttu-id="c7bc3-111">如果這個屬性不存在，為了回溯相容性，此值 **會 \_ \_ \_ 直接** 適用于支援 Alpha 通道的影片格式（例如 ARGB32），或在不含 ALPHA 色板的影片格式（例如 RGB32） **\_ \_ \_ 略** 過。</span><span class="sxs-lookup"><span data-stu-id="c7bc3-111">If this attribute isn’t present, for backward compatibility, the value is **DXGI\_ALPHA\_MODE\_STRAIGHT** for video format supporting alpha channel, such as ARGB32, or **DXGI\_ALPHA\_MODE\_IGNORE** for video format without alpha channel, such as RGB32.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7bc3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7bc3-112">Requirements</span></span>



| <span data-ttu-id="c7bc3-113">需求</span><span class="sxs-lookup"><span data-stu-id="c7bc3-113">Requirement</span></span> | <span data-ttu-id="c7bc3-114">值</span><span class="sxs-lookup"><span data-stu-id="c7bc3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7bc3-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7bc3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c7bc3-116">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7bc3-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c7bc3-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7bc3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c7bc3-118">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7bc3-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="c7bc3-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c7bc3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7bc3-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7bc3-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 

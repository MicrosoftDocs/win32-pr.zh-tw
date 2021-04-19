---
description: 表示畫面格來源類型。
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: 'MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992014"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a><span data-ttu-id="a4b46-103">MF \_ DEVICESTREAM \_ 屬性 \_ FRAMESOURCE \_ 類型屬性</span><span class="sxs-lookup"><span data-stu-id="a4b46-103">MF\_DEVICESTREAM\_ATTRIBUTE\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="a4b46-104">表示畫面格來源類型。</span><span class="sxs-lookup"><span data-stu-id="a4b46-104">Represents the frame source type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a4b46-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a4b46-105">Data type</span></span>

<span data-ttu-id="a4b46-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a4b46-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b46-107">備註</span><span class="sxs-lookup"><span data-stu-id="a4b46-107">Remarks</span></span>

<span data-ttu-id="a4b46-108">這個屬性的值應該是 [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) 列舉中一或多個值的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="a4b46-108">This value of this attribute should be a bitmask of one or more values from the [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) enumeration.</span></span> <span data-ttu-id="a4b46-109">為了支援回溯相容性，當未針對媒體類型定義此屬性時，會假設其值為 **MFFrameSourceTypes：： Color**。</span><span class="sxs-lookup"><span data-stu-id="a4b46-109">To support backward compatibility, when this attribute is not defined for a media type, it is assumed to have the value **MFFrameSourceTypes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b46-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4b46-110">Requirements</span></span>



| <span data-ttu-id="a4b46-111">需求</span><span class="sxs-lookup"><span data-stu-id="a4b46-111">Requirement</span></span> | <span data-ttu-id="a4b46-112">值</span><span class="sxs-lookup"><span data-stu-id="a4b46-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b46-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4b46-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b46-114">Windows 10， \[ 僅限1607版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4b46-114">Windows 10, version 1607 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a4b46-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4b46-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b46-116">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4b46-116">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a4b46-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a4b46-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4b46-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b46-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 





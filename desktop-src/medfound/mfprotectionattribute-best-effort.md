---
description: 設定為 IMFOutputSchema 物件的屬性。
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: 'MFPROTECTIONATTRIBUTE_BEST_EFFORT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192163"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a><span data-ttu-id="4c724-103">MFPROTECTIONATTRIBUTE \_ 最佳 \_ 投入時間屬性</span><span class="sxs-lookup"><span data-stu-id="4c724-103">MFPROTECTIONATTRIBUTE\_BEST\_EFFORT attribute</span></span>

<span data-ttu-id="4c724-104">設定為 [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="4c724-104">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span> <span data-ttu-id="4c724-105">如果有這個屬性，則會忽略嘗試套用保護的嘗試失敗。</span><span class="sxs-lookup"><span data-stu-id="4c724-105">If this attribute is present, a failed attempt to apply the protection is ignored.</span></span> <span data-ttu-id="4c724-106">如果相關聯的屬性值為 **TRUE**，則應該套用具有 [MFPROTECTIONATTRIBUTE \_ 故障 \_ 轉移](mfprotectionattribute-fail-over.md) 屬性的保護架構。</span><span class="sxs-lookup"><span data-stu-id="4c724-106">If the associated attribute value is **TRUE**, the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute should be applied.</span></span>

## <a name="data-type"></a><span data-ttu-id="4c724-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="4c724-107">Data type</span></span>

<span data-ttu-id="4c724-108">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="4c724-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4c724-109">備註</span><span class="sxs-lookup"><span data-stu-id="4c724-109">Remarks</span></span>

<span data-ttu-id="4c724-110">若 **為 TRUE**，如果設定此保護失敗，請使用 [MFPROTECTIONATTRIBUTE \_ 故障 \_ 轉移](mfprotectionattribute-fail-over.md) 屬性來強制執行保護架構。</span><span class="sxs-lookup"><span data-stu-id="4c724-110">If **TRUE**, enforce the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute if setting this protection fails.</span></span>

<span data-ttu-id="4c724-111">設定為 [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="4c724-111">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c724-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c724-112">Requirements</span></span>



| <span data-ttu-id="4c724-113">需求</span><span class="sxs-lookup"><span data-stu-id="4c724-113">Requirement</span></span> | <span data-ttu-id="4c724-114">值</span><span class="sxs-lookup"><span data-stu-id="4c724-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c724-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c724-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4c724-116">\[僅 Windows 8 UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c724-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4c724-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c724-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4c724-118">僅限 Windows Server 2012 \[ UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c724-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4c724-119">標頭</span><span class="sxs-lookup"><span data-stu-id="4c724-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c724-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c724-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c724-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c724-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c724-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4c724-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c724-123">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="4c724-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 





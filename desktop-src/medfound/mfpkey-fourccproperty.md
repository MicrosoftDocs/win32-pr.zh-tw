---
description: 指定可識別您要使用之編碼器的 FOURCC。
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: 'MFPKEY_FOURCC 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943914"
---
# <a name="mfpkey_fourcc-property"></a><span data-ttu-id="ab0bc-103">MFPKEY \_ FOURCC 屬性</span><span class="sxs-lookup"><span data-stu-id="ab0bc-103">MFPKEY\_FOURCC Property</span></span>

<span data-ttu-id="ab0bc-104">指定可識別您要使用之編碼器的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="ab0bc-104">Specifies the FOURCC that identifies the encoder you want to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ab0bc-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="ab0bc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ab0bc-106">g \_ wszWMVCFOURCC</span><span class="sxs-lookup"><span data-stu-id="ab0bc-106">g\_wszWMVCFOURCC</span></span>

## <a name="data-type"></a><span data-ttu-id="ab0bc-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="ab0bc-107">Data Type</span></span>

<span data-ttu-id="ab0bc-108">VT \_ I4 (FOURCC 值) </span><span class="sxs-lookup"><span data-stu-id="ab0bc-108">VT\_I4 (FOURCC value)</span></span>

## <a name="remarks"></a><span data-ttu-id="ab0bc-109">備註</span><span class="sxs-lookup"><span data-stu-id="ab0bc-109">Remarks</span></span>

<span data-ttu-id="ab0bc-110">您必須在使用 **IPropertyBag** 或 **IPropertyStore** 來抓取下列屬性的值之前，先設定此值：</span><span class="sxs-lookup"><span data-stu-id="ab0bc-110">You must set this value before retrieving the values for the following properties using **IPropertyBag** or **IPropertyStore**:</span></span>

-   [<span data-ttu-id="ab0bc-111">MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE</span><span class="sxs-lookup"><span data-stu-id="ab0bc-111">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE</span></span>](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [<span data-ttu-id="ab0bc-112">MFPKEY \_ PASSESRECOMMENDED</span><span class="sxs-lookup"><span data-stu-id="ab0bc-112">MFPKEY\_PASSESRECOMMENDED</span></span>](mfpkey-passesrecommendedproperty.md)

<span data-ttu-id="ab0bc-113">您應該使用 [**IWMCodecProps：： GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) 來取出先前所列之 FOURCC 相依屬性的值。</span><span class="sxs-lookup"><span data-stu-id="ab0bc-113">You should use [**IWMCodecProps::GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) to retrieve the values of the FOURCC-dependent properties listed previously.</span></span> <span data-ttu-id="ab0bc-114">使用 **GetCodecProp** 時，您不需要設定 **MFPKEY \_ FOURCC**。</span><span class="sxs-lookup"><span data-stu-id="ab0bc-114">When using **GetCodecProp**, you do not need to set **MFPKEY\_FOURCC**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab0bc-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab0bc-115">Requirements</span></span>



| <span data-ttu-id="ab0bc-116">需求</span><span class="sxs-lookup"><span data-stu-id="ab0bc-116">Requirement</span></span> | <span data-ttu-id="ab0bc-117">值</span><span class="sxs-lookup"><span data-stu-id="ab0bc-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0bc-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab0bc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ab0bc-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab0bc-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ab0bc-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab0bc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ab0bc-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab0bc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab0bc-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ab0bc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab0bc-123"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab0bc-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab0bc-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab0bc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab0bc-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="ab0bc-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 





---
description: 以位元組為單位，指定用來儲存壓縮內容的容器所需的額外負荷（以位元組為單位）。
ms.assetid: 73ec52de-c74a-45b3-a453-7f32510b4484
title: 'MFPKEY_ASFOVERHEADPERFRAME 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 208acf55871b18bb029279a27abd36a33ea8c79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975498"
---
# <a name="mfpkey_asfoverheadperframe-property"></a><span data-ttu-id="1622f-103">MFPKEY \_ ASFOVERHEADPERFRAME 屬性</span><span class="sxs-lookup"><span data-stu-id="1622f-103">MFPKEY\_ASFOVERHEADPERFRAME Property</span></span>

<span data-ttu-id="1622f-104">以位元組為單位，指定用來儲存壓縮內容的容器所需的額外負荷（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1622f-104">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1622f-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="1622f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1622f-106">g \_ wszWMVPacketOverhead</span><span class="sxs-lookup"><span data-stu-id="1622f-106">g\_wszWMVPacketOverhead</span></span>

## <a name="data-type"></a><span data-ttu-id="1622f-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="1622f-107">Data Type</span></span>

<span data-ttu-id="1622f-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1622f-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1622f-109">預設值</span><span class="sxs-lookup"><span data-stu-id="1622f-109">Default Value</span></span>

<span data-ttu-id="1622f-110">17</span><span class="sxs-lookup"><span data-stu-id="1622f-110">17</span></span>

## <a name="remarks"></a><span data-ttu-id="1622f-111">備註</span><span class="sxs-lookup"><span data-stu-id="1622f-111">Remarks</span></span>

<span data-ttu-id="1622f-112">如果您使用 Advanced Systems 格式 (ASF) 檔案結構，請勿變更此值的預設值。</span><span class="sxs-lookup"><span data-stu-id="1622f-112">If you are using the Advanced Systems Format (ASF) file structure, do not change this value from its default.</span></span> <span data-ttu-id="1622f-113">如果您不是將資料儲存在 ASF 檔案中，則必須將此值設定為0。</span><span class="sxs-lookup"><span data-stu-id="1622f-113">If you are not storing the data in an ASF file, you must set this value to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="1622f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1622f-114">Requirements</span></span>



| <span data-ttu-id="1622f-115">需求</span><span class="sxs-lookup"><span data-stu-id="1622f-115">Requirement</span></span> | <span data-ttu-id="1622f-116">值</span><span class="sxs-lookup"><span data-stu-id="1622f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1622f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1622f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1622f-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1622f-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1622f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1622f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1622f-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1622f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1622f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1622f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1622f-122"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1622f-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1622f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1622f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1622f-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="1622f-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 





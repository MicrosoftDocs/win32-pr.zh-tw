---
description: 指定編碼期間卸載的影片框架數目。
ms.assetid: e55db53e-ab70-42ce-b5cd-2e59a4e96b7b
title: 'MFPKEY_DROPPEDFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31404218e4e179e19f53e30f5750976c71e0d7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692415"
---
# <a name="mfpkey_droppedframes-property"></a><span data-ttu-id="3ca33-103">MFPKEY \_ DROPPEDFRAMES 屬性</span><span class="sxs-lookup"><span data-stu-id="3ca33-103">MFPKEY\_DROPPEDFRAMES Property</span></span>

<span data-ttu-id="3ca33-104">指定編碼期間卸載的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="3ca33-104">Specifies the number of video frames dropped during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3ca33-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="3ca33-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3ca33-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="3ca33-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="3ca33-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="3ca33-107">Data Type</span></span>

<span data-ttu-id="3ca33-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3ca33-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca33-109">備註</span><span class="sxs-lookup"><span data-stu-id="3ca33-109">Remarks</span></span>

<span data-ttu-id="3ca33-110">在編碼期間，有時會略過或捨棄影片框架，因為緩衝區有限制。</span><span class="sxs-lookup"><span data-stu-id="3ca33-110">Video frames are sometimes skipped, or dropped, during encoding because of buffer restrictions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca33-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ca33-111">Requirements</span></span>



| <span data-ttu-id="3ca33-112">需求</span><span class="sxs-lookup"><span data-stu-id="3ca33-112">Requirement</span></span> | <span data-ttu-id="3ca33-113">值</span><span class="sxs-lookup"><span data-stu-id="3ca33-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca33-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ca33-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca33-115">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ca33-115">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3ca33-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ca33-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca33-117">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ca33-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ca33-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3ca33-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ca33-119"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ca33-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ca33-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ca33-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca33-121">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="3ca33-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

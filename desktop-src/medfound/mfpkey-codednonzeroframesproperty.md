---
description: 指定實際包含資料之編解碼器所編碼的影片框架數目。
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: 'MFPKEY_CODEDNONZEROFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987516"
---
# <a name="mfpkey_codednonzeroframes-property"></a><span data-ttu-id="712e0-103">MFPKEY \_ CODEDNONZEROFRAMES 屬性</span><span class="sxs-lookup"><span data-stu-id="712e0-103">MFPKEY\_CODEDNONZEROFRAMES Property</span></span>

<span data-ttu-id="712e0-104">指定實際包含資料之編解碼器所編碼的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="712e0-104">Specifies the number of video frames encoded by the codec that actually contain data.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="712e0-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="712e0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="712e0-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="712e0-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="712e0-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="712e0-107">Data Type</span></span>

<span data-ttu-id="712e0-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="712e0-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="712e0-109">備註</span><span class="sxs-lookup"><span data-stu-id="712e0-109">Remarks</span></span>

<span data-ttu-id="712e0-110">這個值等於 [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) 減去由於位速率限制而捨棄的任何框架，減去任何零位元組的框架。</span><span class="sxs-lookup"><span data-stu-id="712e0-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints, minus any zero-byte frames.</span></span> <span data-ttu-id="712e0-111">完成傳遞範例之後，您可以取得此值。</span><span class="sxs-lookup"><span data-stu-id="712e0-111">You can get this value after you are finished passing samples.</span></span> <span data-ttu-id="712e0-112">可以為重複的框架建立零位元組的框架。</span><span class="sxs-lookup"><span data-stu-id="712e0-112">Zero-byte frames can be created for duplicate frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="712e0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="712e0-113">Requirements</span></span>



| <span data-ttu-id="712e0-114">需求</span><span class="sxs-lookup"><span data-stu-id="712e0-114">Requirement</span></span> | <span data-ttu-id="712e0-115">值</span><span class="sxs-lookup"><span data-stu-id="712e0-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="712e0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="712e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="712e0-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="712e0-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="712e0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="712e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="712e0-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="712e0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="712e0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="712e0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="712e0-121"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="712e0-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="712e0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="712e0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="712e0-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="712e0-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 

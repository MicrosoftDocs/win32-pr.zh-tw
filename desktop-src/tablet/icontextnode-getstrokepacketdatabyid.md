---
description: 取得陣列，其中包含指定之筆劃的封包屬性資料。
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'ICoNtextNode：： GetStrokePacketDataById 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995821"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a><span data-ttu-id="00381-103">ICoNtextNode：： GetStrokePacketDataById 方法</span><span class="sxs-lookup"><span data-stu-id="00381-103">IContextNode::GetStrokePacketDataById method</span></span>

<span data-ttu-id="00381-104">取得陣列，其中包含指定之筆劃的封包屬性資料。</span><span class="sxs-lookup"><span data-stu-id="00381-104">Retrieves an array containing the packet property data for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="00381-105">語法</span><span class="sxs-lookup"><span data-stu-id="00381-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="00381-106">參數</span><span class="sxs-lookup"><span data-stu-id="00381-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00381-107">*strokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00381-107">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00381-108">筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="00381-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="00381-109">*pStrokePacketDataCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="00381-109">*pStrokePacketDataCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="00381-110">封包資料陣列的長度。</span><span class="sxs-lookup"><span data-stu-id="00381-110">The length of the packet data array.</span></span>

</dd> <dt>

<span data-ttu-id="00381-111">*pplStrokePacketData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="00381-111">*pplStrokePacketData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00381-112">筆劃的封包資料指標。</span><span class="sxs-lookup"><span data-stu-id="00381-112">A pointer to the packet data for the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00381-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="00381-113">Return value</span></span>

<span data-ttu-id="00381-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="00381-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="00381-115">備註</span><span class="sxs-lookup"><span data-stu-id="00381-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="00381-116">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *pplStrokePacketData* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="00381-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokePacketData* when you no longer need the information.</span></span>

 

<span data-ttu-id="00381-117">*plStrokePacketData* 包含筆劃中所有點的封包資料。</span><span class="sxs-lookup"><span data-stu-id="00381-117">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="00381-118">若要取得筆劃中每個點所包含的封包資料類型，請使用 [**ICoNtextNode：： GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)。</span><span class="sxs-lookup"><span data-stu-id="00381-118">To get the types of packet data included for each point in the stroke, use [**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00381-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="00381-119">Requirements</span></span>



| <span data-ttu-id="00381-120">需求</span><span class="sxs-lookup"><span data-stu-id="00381-120">Requirement</span></span> | <span data-ttu-id="00381-121">值</span><span class="sxs-lookup"><span data-stu-id="00381-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00381-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00381-122">Minimum supported client</span></span><br/> | <span data-ttu-id="00381-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00381-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="00381-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00381-124">Minimum supported server</span></span><br/> | <span data-ttu-id="00381-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="00381-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="00381-126">標頭</span><span class="sxs-lookup"><span data-stu-id="00381-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="00381-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="00381-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="00381-128">DLL</span><span class="sxs-lookup"><span data-stu-id="00381-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00381-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00381-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="00381-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00381-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00381-131">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="00381-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="00381-132">**ICoNtextNode::GetStrokePacketDescriptionById**</span><span class="sxs-lookup"><span data-stu-id="00381-132">**IContextNode::GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[<span data-ttu-id="00381-133">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="00381-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


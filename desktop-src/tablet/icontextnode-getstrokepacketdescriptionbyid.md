---
description: 取得陣列，其中包含指定之筆劃的封包屬性識別碼。
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'ICoNtextNode：： GetStrokePacketDescriptionById 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970623"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a><span data-ttu-id="d3cf2-103">ICoNtextNode：： GetStrokePacketDescriptionById 方法</span><span class="sxs-lookup"><span data-stu-id="d3cf2-103">IContextNode::GetStrokePacketDescriptionById method</span></span>

<span data-ttu-id="d3cf2-104">取得陣列，其中包含指定之筆劃的封包屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3cf2-104">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3cf2-105">語法</span><span class="sxs-lookup"><span data-stu-id="d3cf2-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a><span data-ttu-id="d3cf2-106">參數</span><span class="sxs-lookup"><span data-stu-id="d3cf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3cf2-107">*lStrokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3cf2-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3cf2-108">筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3cf2-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="d3cf2-109">*pulStrokePacketDescriptionCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d3cf2-109">*pulStrokePacketDescriptionCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3cf2-110">每個封包中的封包屬性數目。</span><span class="sxs-lookup"><span data-stu-id="d3cf2-110">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="d3cf2-111">*ppStrokePacketDescriptionGuids* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d3cf2-111">*ppStrokePacketDescriptionGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3cf2-112">陣列，包含封包屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3cf2-112">An array containing the packet property identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3cf2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3cf2-113">Return value</span></span>

<span data-ttu-id="d3cf2-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="d3cf2-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3cf2-115">備註</span><span class="sxs-lookup"><span data-stu-id="d3cf2-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="d3cf2-116">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppStrokePacketDescriptionGuids* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d3cf2-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppStrokePacketDescriptionGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="d3cf2-117">\**ppStrokePacketDescriptionGuids* 包含 (guid) 的全域唯一識別碼，描述筆劃中每個點所包含的封包資料類型。</span><span class="sxs-lookup"><span data-stu-id="d3cf2-117">\**ppStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="d3cf2-118">如需可用的封包屬性完整清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="d3cf2-118">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3cf2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3cf2-119">Requirements</span></span>



| <span data-ttu-id="d3cf2-120">需求</span><span class="sxs-lookup"><span data-stu-id="d3cf2-120">Requirement</span></span> | <span data-ttu-id="d3cf2-121">值</span><span class="sxs-lookup"><span data-stu-id="d3cf2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3cf2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3cf2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d3cf2-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3cf2-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d3cf2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3cf2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d3cf2-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="d3cf2-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d3cf2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d3cf2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3cf2-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d3cf2-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d3cf2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d3cf2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3cf2-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3cf2-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d3cf2-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3cf2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3cf2-131">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="d3cf2-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d3cf2-132">**ICoNtextNode::GetStrokePacketDataById**</span><span class="sxs-lookup"><span data-stu-id="d3cf2-132">**IContextNode::GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[<span data-ttu-id="d3cf2-133">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="d3cf2-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


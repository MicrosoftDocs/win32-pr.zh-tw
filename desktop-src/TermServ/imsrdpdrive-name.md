---
title: IMsRdpDrive Name 屬性
description: 抓取磁片磁碟機的名稱。
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Name 屬性遠端桌面服務
- Name 屬性遠端桌面服務，IMsRdpDrive 介面
- IMsRdpDrive 介面遠端桌面服務，Name 屬性
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38eeb0f6112983f508bb43ba69d721aeb52c314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465989"
---
# <a name="imsrdpdrivename-property"></a><span data-ttu-id="0a610-106">IMsRdpDrive：： Name 屬性</span><span class="sxs-lookup"><span data-stu-id="0a610-106">IMsRdpDrive::Name property</span></span>

<span data-ttu-id="0a610-107">抓取磁片磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a610-107">Retrieves the name of the drive.</span></span>

<span data-ttu-id="0a610-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0a610-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a610-109">語法</span><span class="sxs-lookup"><span data-stu-id="0a610-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a><span data-ttu-id="0a610-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="0a610-110">Property value</span></span>

<span data-ttu-id="0a610-111">磁片磁碟機名稱。</span><span class="sxs-lookup"><span data-stu-id="0a610-111">The drive name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0a610-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0a610-112">Error codes</span></span>

<span data-ttu-id="0a610-113">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="0a610-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="0a610-114">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="0a610-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a610-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a610-115">Requirements</span></span>



| <span data-ttu-id="0a610-116">需求</span><span class="sxs-lookup"><span data-stu-id="0a610-116">Requirement</span></span> | <span data-ttu-id="0a610-117">值</span><span class="sxs-lookup"><span data-stu-id="0a610-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a610-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a610-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0a610-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a610-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0a610-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a610-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0a610-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a610-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0a610-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0a610-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a610-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a610-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a610-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0a610-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a610-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a610-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a610-126">IID</span><span class="sxs-lookup"><span data-stu-id="0a610-126">IID</span></span><br/>                      | <span data-ttu-id="0a610-127">IID \_ IMsRdpDrive 定義為 d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="0a610-127">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="0a610-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a610-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a610-129">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="0a610-129">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 






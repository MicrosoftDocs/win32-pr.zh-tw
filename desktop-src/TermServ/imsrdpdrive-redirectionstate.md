---
title: IMsRdpDrive RedirectionState 屬性
description: 指出磁片磁碟機的重新導向狀態。
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- RedirectionState 屬性遠端桌面服務
- RedirectionState 屬性遠端桌面服務，IMsRdpDrive 介面
- IMsRdpDrive 介面遠端桌面服務，RedirectionState 屬性
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561190e976e0b8190553376f5e9f7a5b2de2550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384985"
---
# <a name="imsrdpdriveredirectionstate-property"></a><span data-ttu-id="9333d-106">IMsRdpDrive：： RedirectionState 屬性</span><span class="sxs-lookup"><span data-stu-id="9333d-106">IMsRdpDrive::RedirectionState property</span></span>

<span data-ttu-id="9333d-107">指出磁片磁碟機的重新導向狀態。</span><span class="sxs-lookup"><span data-stu-id="9333d-107">Indicates the redirection state of the drive.</span></span>

<span data-ttu-id="9333d-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9333d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9333d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9333d-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="9333d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="9333d-110">Property value</span></span>

<span data-ttu-id="9333d-111">將此參數設定為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9333d-111">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="9333d-112">停用重新導向或 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9333d-112">to disable redirection or **VARIANT\_TRUE**.</span></span> <span data-ttu-id="9333d-113">啟用重新導向。</span><span class="sxs-lookup"><span data-stu-id="9333d-113">to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9333d-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9333d-114">Error codes</span></span>

<span data-ttu-id="9333d-115">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="9333d-115">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="9333d-116">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="9333d-116">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9333d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9333d-117">Requirements</span></span>



| <span data-ttu-id="9333d-118">需求</span><span class="sxs-lookup"><span data-stu-id="9333d-118">Requirement</span></span> | <span data-ttu-id="9333d-119">值</span><span class="sxs-lookup"><span data-stu-id="9333d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9333d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9333d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9333d-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9333d-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9333d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9333d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9333d-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9333d-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9333d-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9333d-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="9333d-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9333d-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9333d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9333d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9333d-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9333d-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9333d-128">IID</span><span class="sxs-lookup"><span data-stu-id="9333d-128">IID</span></span><br/>                      | <span data-ttu-id="9333d-129">IID \_ IMsRdpDrive 定義為 d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="9333d-129">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="9333d-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9333d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9333d-131">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="9333d-131">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





